<template>
  <div class="w-full lg:w-1/3 mt-6 lg:mt-0 text-center space-y-6" v-bind="$attrs">
    <div class="w-full">
      <h3 class="text-lg font-semibold text-gray-800 mb-2">{{ title }}</h3>
      <p class="text-sm text-gray-600">{{ subtitle }}</p>
    </div>
    
    <div class="space-y-4">
      <div v-for="stat in stats" :key="stat.id" class="bg-white rounded-lg p-6 shadow-sm border border-gray-100">
        <div class="flex items-center justify-center space-x-3 mb-3">
          <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center">
            <Icon :icon="stat.icon" :size="24" class="text-blue-600" />
          </div>
          <div class="text-center">
            <div class="text-3xl font-bold text-gray-900" ref="numberRef">
              {{ stat.value }}
            </div>
            <div class="text-sm text-gray-600">{{ stat.label }}</div>
          </div>
        </div>
        
        <div class="flex items-center justify-center space-x-1">
          <Icon 
            :icon="stat.increase ? 'mdi-trending-up' : 'mdi-trending-down'" 
            :size="16" 
            :class="stat.increase ? 'text-green-500' : 'text-red-500'" 
          />
          <span class="text-xs" :class="stat.increase ? 'text-green-600' : 'text-red-600'">
            {{ stat.change }}
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LandingSimpleStatistic',
  props: {
    title: {
      type: String,
      default: '',
    },
    subtitle: {
      type: String,
      default: '',
    },
    stats: {
      type: Array,
      default: () => [],
    },
  },
  mounted() {
    this.animateNumbers()
  },
  methods: {
    animateNumbers() {
      const numberElements = this.$refs.numberRef
      if (!numberElements) return
      
      const elements = Array.isArray(numberElements) ? numberElements : [numberElements]
      
      elements.forEach((element, index) => {
        const stat = this.stats[index]
        if (!stat || !element) return
        
        const finalValue = stat.value
        const duration = 2000
        const startTime = Date.now()
        
        const animate = () => {
          const currentTime = Date.now()
          const elapsed = currentTime - startTime
          const progress = Math.min(elapsed / duration, 1)
          
          // Easing function for smooth animation
          const easeOutQuart = 1 - Math.pow(1 - progress, 4)
          const currentValue = finalValue * easeOutQuart
          
          // Format the number based on whether it's a decimal or integer
          if (Number.isInteger(finalValue)) {
            element.textContent = Math.floor(currentValue)
          } else {
            element.textContent = currentValue.toFixed(1)
          }
          
          if (progress < 1) {
            requestAnimationFrame(animate)
          }
        }
        
        // Start animation when element is in viewport
        const observer = new IntersectionObserver((entries) => {
          entries.forEach(entry => {
            if (entry.isIntersecting) {
              animate()
              observer.unobserve(entry.target)
            }
          })
        })
        
        observer.observe(element)
      })
    }
  }
}
</script> 