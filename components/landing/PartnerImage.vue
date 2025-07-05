<template>
  <div class="flex items-center justify-center p-6">
    <div class="w-32 h-32 bg-white rounded-lg shadow-md flex items-center justify-center border border-gray-200 hover:shadow-lg transition-all duration-300">
      <Icon 
        :icon="getPartnerIcon(img)" 
        class="text-[#1A3E7F]" 
        :size="48" 
      />
    </div>
  </div>
</template>
<script>
export default {
  props: {
    img: {
      type: String,
      default: '',
    },
  },
  methods: {
    getPartnerIcon(img) {
      const iconMap = {
        'clever.png': 'mdi-hospital-building',
        'diamon-cutts.png': 'mdi-medical-bag',
        'swiss-finance.png': 'mdi-stethoscope',
        'gambio.png': 'mdi-doctor'
      }
      return iconMap[img] || 'mdi-hospital'
    }
  }
}
</script>
