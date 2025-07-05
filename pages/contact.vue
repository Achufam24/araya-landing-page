<template>
  <div class="w-full">
    <!-- Hero section -->
    <section class="w-full py-16 bg-gradient-to-br from-blue-50 to-blue-100">
      <div class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
          <span class="text-base text-gradient font-semibold uppercase mb-4">Get in Touch</span>
          <h1 class="text-4xl sm:text-5xl font-bold text-gray-900 mb-6">
            Contact <span class="text-header-gradient">Araya</span> Support
          </h1>
          <p class="text-xl text-gray-600 max-w-3xl mx-auto">
            Our dedicated support team is here to help you with any questions about our telemedicine services.
          </p>
        </div>
      </div>
    </section>

    <!-- Contact methods section -->
    <section class="w-full py-16">
      <div class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
          <!-- 24/7 Support -->
          <div class="bg-white p-8 rounded-2xl shadow-lg border border-gray-100">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mb-6">
              <Icon icon="mdi-headset" class="text-green-600" :size="32" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-4">24/7 Live Support</h3>
            <p class="text-gray-600 mb-6">
              Get immediate help from our medical support team. Available around the clock for urgent care questions.
            </p>
            <BaseButton class="w-full px-6 py-3 bg-green-600 text-white hover:bg-green-700 transition-all duration-300">
              Start Live Chat
            </BaseButton>
          </div>

          <!-- Phone Support -->
          <div class="bg-white p-8 rounded-2xl shadow-lg border border-gray-100">
            <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
              <Icon icon="mdi-phone" class="text-blue-600" :size="32" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-4">Phone Support</h3>
            <p class="text-gray-600 mb-6">
              Speak directly with our customer service team. We're here to help with account and billing questions.
            </p>
            <div class="space-y-2">
              <p class="text-2xl font-bold text-blue-600">1-800-ARAYA-1</p>
              <p class="text-sm text-gray-500">Mon-Fri: 8AM-8PM EST</p>
            </div>
          </div>

          <!-- Email Support -->
          <div class="bg-white p-8 rounded-2xl shadow-lg border border-gray-100">
            <div class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mb-6">
              <Icon icon="mdi-email" class="text-purple-600" :size="32" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-4">Email Support</h3>
            <p class="text-gray-600 mb-6">
              Send us a detailed message and we'll respond within 24 hours with comprehensive assistance.
            </p>
            <BaseButton class="w-full px-6 py-3 bg-purple-600 text-white hover:bg-purple-700 transition-all duration-300">
              Send Email
            </BaseButton>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact form section -->
    <section class="w-full py-16 bg-gray-50">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-12">
          <h2 class="text-3xl font-bold text-gray-900 mb-4">Send us a Message</h2>
          <p class="text-gray-600">
            Fill out the form below and we'll get back to you as soon as possible.
          </p>
        </div>

        <div class="bg-white rounded-2xl shadow-lg p-8">
          <form @submit.prevent="submitForm" class="space-y-6">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div>
                <label class="block text-sm font-medium text-gray-700 mb-2">First Name</label>
                <input
                  v-model="form.firstName"
                  type="text"
                  required
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#1A3E7F] focus:border-transparent"
                  placeholder="Enter your first name"
                />
              </div>
              <div>
                <label class="block text-sm font-medium text-gray-700 mb-2">Last Name</label>
                <input
                  v-model="form.lastName"
                  type="text"
                  required
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#1A3E7F] focus:border-transparent"
                  placeholder="Enter your last name"
                />
              </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div>
                <label class="block text-sm font-medium text-gray-700 mb-2">Email Address</label>
                <input
                  v-model="form.email"
                  type="email"
                  required
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#1A3E7F] focus:border-transparent"
                  placeholder="Enter your email address"
                />
              </div>
              <div>
                <label class="block text-sm font-medium text-gray-700 mb-2">Phone Number</label>
                <input
                  v-model="form.phone"
                  type="tel"
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#1A3E7F] focus:border-transparent"
                  placeholder="Enter your phone number"
                />
              </div>
            </div>

            <div>
              <label class="block text-sm font-medium text-gray-700 mb-2">Subject</label>
              <select
                v-model="form.subject"
                required
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#1A3E7F] focus:border-transparent"
              >
                <option value="">Select a subject</option>
                <option value="general">General Inquiry</option>
                <option value="technical">Technical Support</option>
                <option value="billing">Billing Question</option>
                <option value="medical">Medical Question</option>
                <option value="account">Account Issue</option>
                <option value="feedback">Feedback</option>
              </select>
            </div>

            <div>
              <label class="block text-sm font-medium text-gray-700 mb-2">Message</label>
              <textarea
                v-model="form.message"
                required
                rows="6"
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#1A3E7F] focus:border-transparent"
                placeholder="Please describe your inquiry in detail..."
              ></textarea>
            </div>

            <div class="flex items-center">
              <input
                v-model="form.agree"
                type="checkbox"
                required
                class="h-4 w-4 text-[#1A3E7F] focus:ring-[#1A3E7F] border-gray-300 rounded"
              />
              <label class="ml-2 block text-sm text-gray-700">
                I agree to the <a href="/privacy-policy" class="text-[#1A3E7F] hover:underline">Privacy Policy</a> and 
                <a href="#" class="text-[#1A3E7F] hover:underline">Terms of Service</a>
              </label>
            </div>

            <div class="text-center">
              <BaseButton
                type="submit"
                :disabled="isSubmitting"
                class="px-8 py-4 bg-gradient-to-r from-[#1A3E7F] to-[#2B5AA0] text-white hover:shadow-lg transition-all duration-300 disabled:opacity-50"
              >
                <span v-if="isSubmitting" class="flex items-center">
                  <Icon icon="mdi-loading" class="animate-spin mr-2" :size="20" />
                  Sending...
                </span>
                <span v-else>Send Message</span>
              </BaseButton>
            </div>
          </form>
        </div>
      </div>
    </section>

    <!-- FAQ section -->
    <section class="w-full py-16">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-12">
          <h2 class="text-3xl font-bold text-gray-900 mb-4">Frequently Asked Questions</h2>
          <p class="text-gray-600">
            Quick answers to common questions about contacting Araya support.
          </p>
        </div>

        <div class="space-y-4">
          <div class="bg-white rounded-lg border border-gray-200">
            <button
              @click="toggleFAQ(1)"
              class="w-full px-6 py-4 text-left flex justify-between items-center hover:bg-gray-50"
            >
              <span class="font-medium text-gray-900">How quickly will I receive a response?</span>
              <Icon :icon="openFAQ === 1 ? 'mdi-chevron-up' : 'mdi-chevron-down'" class="text-gray-500" :size="20" />
            </button>
            <div v-if="openFAQ === 1" class="px-6 pb-4">
              <p class="text-gray-600">
                We typically respond to emails within 24 hours. For urgent medical questions, we recommend using our 24/7 live chat or calling our support line.
              </p>
            </div>
          </div>

          <div class="bg-white rounded-lg border border-gray-200">
            <button
              @click="toggleFAQ(2)"
              class="w-full px-6 py-4 text-left flex justify-between items-center hover:bg-gray-50"
            >
              <span class="font-medium text-gray-900">Can I contact support for medical advice?</span>
              <Icon :icon="openFAQ === 2 ? 'mdi-chevron-up' : 'mdi-chevron-down'" class="text-gray-500" :size="20" />
            </button>
            <div v-if="openFAQ === 2" class="px-6 pb-4">
              <p class="text-gray-600">
                For medical advice, please schedule a consultation with one of our licensed healthcare providers through the app. Our support team can help with technical and account-related questions.
              </p>
            </div>
          </div>

          <div class="bg-white rounded-lg border border-gray-200">
            <button
              @click="toggleFAQ(3)"
              class="w-full px-6 py-4 text-left flex justify-between items-center hover:bg-gray-50"
            >
              <span class="font-medium text-gray-900">What information should I include in my message?</span>
              <Icon :icon="openFAQ === 3 ? 'mdi-chevron-up' : 'mdi-chevron-down'" class="text-gray-500" :size="20" />
            </button>
            <div v-if="openFAQ === 3" class="px-6 pb-4">
              <p class="text-gray-600">
                Please include your account email, a clear description of your issue, and any relevant screenshots or error messages. This helps us provide faster and more accurate assistance.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import aosMixin from '@/mixins/aos'

export default {
  name: 'ContactPage',
  mixins: [aosMixin],
  data() {
    return {
      openFAQ: null,
      isSubmitting: false,
      form: {
        firstName: '',
        lastName: '',
        email: '',
        phone: '',
        subject: '',
        message: '',
        agree: false
      }
    }
  },
  methods: {
    toggleFAQ(id) {
      this.openFAQ = this.openFAQ === id ? null : id
    },
    async submitForm() {
      this.isSubmitting = true
      
      // Simulate form submission
      await new Promise(resolve => setTimeout(resolve, 2000))
      
      // Reset form
      this.form = {
        firstName: '',
        lastName: '',
        email: '',
        phone: '',
        subject: '',
        message: '',
        agree: false
      }
      
      this.isSubmitting = false
      
      // Show success message (you can implement a toast notification here)
      alert('Thank you for your message! We will get back to you within 24 hours.')
    }
  }
}
</script>

<style scoped>
.text-header-gradient {
  background: rgb(26, 62, 127);
  background: linear-gradient(169.4deg, #1A3E7F -6.01%, #2B5AA0 36.87%, #4A8FF6 78.04%, #6BA3FF 103.77%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

.text-gradient {
  background: linear-gradient(135deg, #1A3E7F 0%, #2B5AA0 100%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style> 