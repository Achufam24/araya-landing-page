<template>
  <div class="max-w-[280px] xl:max-w-[363px] space-y-6 sm:space-y-3 text-center">
    <div class="w-24 h-24 bg-gradient-to-br from-[#1A3E7F] to-[#2B5AA0] rounded-full flex items-center justify-center mx-auto shadow-lg">
      <Icon 
        :icon="getStepIcon(step.title)" 
        class="text-white" 
        :size="48" 
      />
    </div>
    <h3 class="text-xl text-neutral-800 font-semibold">{{ step.title }}</h3>
    <p class="text-sm text-gray-700 leading-relaxed">
      {{ step.description }}
    </p>
  </div>
</template>
<script>
export default {
  name: 'LandingStep',
  props: {
    step: {
      type: Object,
      required: true,
    },
  },
  methods: {
    getStepIcon(title) {
      const iconMap = {
        'Sign Up': 'mdi-account-plus',
        'Select Care': 'mdi-calendar-check',
        'Get Care': 'mdi-video',
        'Fund': 'mdi-credit-card',
        'Buy Crypto': 'mdi-bitcoin'
      }
      return iconMap[title] || 'mdi-check-circle'
    }
  }
}
</script>
