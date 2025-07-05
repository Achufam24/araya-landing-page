<template>
  <div class="flex items-center space-x-4">
    <div class="lg:max-w-[336px] w-full flex items-center relative px-5 py-3 border border-[#1A3E7F] rounded-xl">
      <span class="text-sm font-medium pr-5 py-3 text-[#1A3E7F] border-r border-[#1A3E7F]"> {{ title }} </span>
      <input
        :type="type"
        class="w-full text-lg font-medium text-right border-none ring-0 focus:outline-none focus:ring-0"
        :name="name"
        :value="defaultValue"
      />
    </div>
    <div class="relative w-full max-w-[106px] sm:max-w-[159px]">
      <button
        type="button"
        class="w-full flex items-center justify-center space-x-1 relative sm:px-6 py-[1.35rem] border border-[#1A3E7F] rounded-xl text-sm font-medium"
        @click="toggleDropdown"
        @blur="toggleDropdown"
      >
        <div class="w-6 h-6 bg-blue-100 rounded-full flex items-center justify-center flex-shrink-0">
          <Icon :icon="getExchangeIcon(exchangeSelected.name)" class="text-[#1A3E7F]" :size="16" />
        </div>
        <span class="ml-3 block truncate">{{ exchangeSelected.name }}</span>
        <ChevronDownIcon :size="20" class="text-[#1A3E7F]" />
      </button>
      <transition name="transform-fade-down">
        <ul
          v-if="openDropdown"
          class="absolute z-10 mt-1 w-full bg-white shadow-lg max-h-56 rounded-md py-1 text-base ring-1 ring-black ring-opacity-5 overflow-auto focus:outline-none sm:text-sm border border-[#1A3E7F]"
          tabindex="-1"
        >
          <li
            v-for="exchange in exchanges"
            id="listbox-option-0"
            :key="exchange.name"
            class="text-gray-900 cursor-default select-none relative px-3 sm:px-5 py-2 hover:bg-blue-50"
            role="option"
          >
            <div class="flex items-center">
              <div class="w-6 h-6 bg-blue-100 rounded-full flex items-center justify-center flex-shrink-0">
                <Icon :icon="getExchangeIcon(exchange.name)" class="text-[#1A3E7F]" :size="16" />
              </div>
              <span class="font-normal ml-3 block truncate"> {{ exchange.name }} </span>
            </div>
          </li>
        </ul>
      </transition>
    </div>
  </div>
</template>
<script>
export default {
  name: 'LandingExchange',
  props: {
    title: {
      type: String,
      default: '',
    },
    name: {
      type: String,
      require: true,
      default: ""
    },
    defaultValue: {
      type: [Number, String],
      default: '',
    },
    exchangeSelected: {
      type: Object,
      required: true,
    },
    exchanges: {
      type: Array,
      required: true,
    },
    type: {
      type: String,
      default: "text"
    }
  },
  data() {
    return {
      openDropdown: false,
    }
  },
  methods: {
    toggleDropdown () {
      this.openDropdown = !this.openDropdown
    },
    getExchangeIcon(name) {
      const iconMap = {
        'General Health': 'mdi-heart-pulse',
        'Pediatrics': 'mdi-baby-face',
        'Mental Health': 'mdi-brain',
        'Dermatology': 'mdi-hand-cream',
        '15 minutes': 'mdi-clock-outline',
        '30 minutes': 'mdi-clock',
        '1 hour': 'mdi-clock-time-four',
        'USD': 'mdi-currency-usd',
        'BTC': 'mdi-bitcoin'
      }
      return iconMap[name] || 'mdi-check-circle'
    }
  }
}
</script>
