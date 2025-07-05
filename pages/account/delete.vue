<template>
  <div class="w-full">
    <!-- Hero section -->
    <section class="w-full py-16 bg-gradient-to-br from-red-50 to-red-100">
      <div class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
          <div class="w-20 h-20 bg-red-100 rounded-full flex items-center justify-center mx-auto mb-6">
            <Icon icon="mdi-alert-circle" class="text-red-600" :size="40" />
          </div>
          <h1 class="text-4xl sm:text-5xl font-bold text-gray-900 mb-6">
            Delete Your <span class="text-red-600">Account</span>
          </h1>
          <p class="text-xl text-gray-600 max-w-3xl mx-auto">
            This action is permanent and cannot be undone. Please read the information below carefully before proceeding.
          </p>
        </div>
      </div>
    </section>

    <!-- Warning section -->
    <section class="w-full py-16">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="bg-red-50 border border-red-200 rounded-2xl p-8 mb-8">
          <div class="flex items-start space-x-4">
            <div class="w-12 h-12 bg-red-100 rounded-full flex items-center justify-center flex-shrink-0">
              <Icon icon="mdi-alert" class="text-red-600" :size="24" />
            </div>
            <div>
              <h3 class="text-xl font-semibold text-red-800 mb-2">Important Warning</h3>
              <p class="text-red-700">
                Deleting your account will permanently remove all your data, including medical records, 
                consultation history, prescriptions, and personal information. This action cannot be undone.
              </p>
            </div>
          </div>
        </div>

        <!-- What will be deleted -->
        <div class="bg-white rounded-2xl shadow-lg p-8 mb-8">
          <h2 class="text-2xl font-bold text-gray-900 mb-6">What will be permanently deleted:</h2>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div class="flex items-start space-x-3">
              <Icon icon="mdi-file-document" class="text-red-500 mt-1" :size="20" />
              <div>
                <h4 class="font-medium text-gray-900">Medical Records</h4>
                <p class="text-sm text-gray-600">All consultation notes and medical history</p>
              </div>
            </div>
            <div class="flex items-start space-x-3">
              <Icon icon="mdi-prescription" class="text-red-500 mt-1" :size="20" />
              <div>
                <h4 class="font-medium text-gray-900">Prescriptions</h4>
                <p class="text-sm text-gray-600">Current and past prescription records</p>
              </div>
            </div>
            <div class="flex items-start space-x-3">
              <Icon icon="mdi-calendar" class="text-red-500 mt-1" :size="20" />
              <div>
                <h4 class="font-medium text-gray-900">Appointment History</h4>
                <p class="text-sm text-gray-600">All past consultations and appointments</p>
              </div>
            </div>
            <div class="flex items-start space-x-3">
              <Icon icon="mdi-account" class="text-red-500 mt-1" :size="20" />
              <div>
                <h4 class="font-medium text-gray-900">Personal Information</h4>
                <p class="text-sm text-gray-600">Profile data and contact information</p>
              </div>
            </div>
            <div class="flex items-start space-x-3">
              <Icon icon="mdi-credit-card" class="text-red-500 mt-1" :size="20" />
              <div>
                <h4 class="font-medium text-gray-900">Payment Information</h4>
                <p class="text-sm text-gray-600">Saved payment methods and billing history</p>
              </div>
            </div>
            <div class="flex items-start space-x-3">
              <Icon icon="mdi-message" class="text-red-500 mt-1" :size="20" />
              <div>
                <h4 class="font-medium text-gray-900">Support Messages</h4>
                <p class="text-sm text-gray-600">All communication with support team</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Before you delete -->
        <div class="bg-blue-50 border border-blue-200 rounded-2xl p-8 mb-8">
          <h2 class="text-2xl font-bold text-gray-900 mb-6">Before you delete your account:</h2>
          <div class="space-y-4">
            <div class="flex items-start space-x-3">
              <Icon icon="mdi-download" class="text-blue-600 mt-1" :size="20" />
              <div>
                <h4 class="font-medium text-gray-900">Download your medical records</h4>
                <p class="text-sm text-gray-600">
                  You can request a copy of your medical records before deletion. 
                  <a href="#" class="text-blue-600 hover:underline">Request medical records</a>
                </p>
              </div>
            </div>
            <div class="flex items-start space-x-3">
              <Icon icon="mdi-cancel" class="text-blue-600 mt-1" :size="20" />
              <div>
                <h4 class="font-medium text-gray-900">Cancel any active subscriptions</h4>
                <p class="text-sm text-gray-600">
                  Ensure you've cancelled any recurring payments to avoid future charges.
                </p>
              </div>
            </div>
            <div class="flex items-start space-x-3">
              <Icon icon="mdi-export" class="text-blue-600 mt-1" :size="20" />
              <div>
                <h4 class="font-medium text-gray-900">Export your data</h4>
                <p class="text-sm text-gray-600">
                  Download a copy of your account data for your records.
                  <a href="#" class="text-blue-600 hover:underline">Export data</a>
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- Confirmation form -->
        <div class="bg-white rounded-2xl shadow-lg p-8">
          <h2 class="text-2xl font-bold text-gray-900 mb-6">Confirm Account Deletion</h2>
          
          <!-- API Error Display -->
          <div v-if="apiError" class="bg-red-50 border border-red-200 rounded-lg p-4 mb-6">
            <div class="flex items-start space-x-3">
              <Icon icon="mdi-alert-circle" class="text-red-600 mt-1" :size="20" />
              <div>
                <h4 class="text-sm font-medium text-red-800">Error</h4>
                <p class="text-sm text-red-700">{{ apiError }}</p>
              </div>
            </div>
          </div>
          
          <form @submit.prevent="confirmDeletion" class="space-y-6">
            <!-- Security verification section -->
            <div class="bg-gray-50 border border-gray-200 rounded-lg p-6 mb-6">
              <h3 class="text-lg font-semibold text-gray-900 mb-4">Security Verification</h3>
              <p class="text-sm text-gray-600 mb-4">
                Please verify your identity by entering your email and password to confirm account deletion.
              </p>
              
              <div class="space-y-4">
                <div>
                  <label class="block text-sm font-medium text-gray-700 mb-2">Email Address</label>
                  <input
                    v-model="form.email"
                    type="email"
                    required
                    class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-transparent"
                    placeholder="Enter your registered email address"
                    :class="{ 'border-red-500': form.email && !isValidEmail }"
                  />
                  <p v-if="form.email && !isValidEmail" class="text-red-500 text-sm mt-1">
                    Please enter a valid email address.
                  </p>
                </div>
                
                <div>
                  <label class="block text-sm font-medium text-gray-700 mb-2">Password</label>
                  <input
                    v-model="form.password"
                    type="password"
                    required
                    class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-transparent"
                    placeholder="Enter your account password"
                  />
                </div>
              </div>
            </div>

            <div>
              <label class="block text-sm font-medium text-gray-700 mb-2">Reason for deletion (optional)</label>
              <select
                v-model="form.reason"
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-transparent"
              >
                <option value="">Select a reason</option>
                <option value="no-longer-needed">No longer needed</option>
                <option value="privacy-concerns">Privacy concerns</option>
                <option value="switching-provider">Switching to another provider</option>
                <option value="technical-issues">Technical issues</option>
                <option value="cost">Cost concerns</option>
                <option value="other">Other</option>
              </select>
            </div>

            <div v-if="form.reason === 'other'">
              <label class="block text-sm font-medium text-gray-700 mb-2">Please specify</label>
              <textarea
                v-model="form.otherReason"
                rows="3"
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-transparent"
                placeholder="Please describe your reason for deleting the account..."
              ></textarea>
            </div>

            <div class="space-y-4">
              <div class="flex items-start space-x-3">
                <input
                  v-model="form.confirmData"
                  type="checkbox"
                  required
                  class="h-4 w-4 text-red-600 focus:ring-red-500 border-gray-300 rounded mt-1"
                />
                <label class="text-sm text-gray-700">
                  I understand that all my data will be permanently deleted and cannot be recovered.
                </label>
              </div>
              
              <div class="flex items-start space-x-3">
                <input
                  v-model="form.confirmMedical"
                  type="checkbox"
                  required
                  class="h-4 w-4 text-red-600 focus:ring-red-500 border-gray-300 rounded mt-1"
                />
                <label class="text-sm text-gray-700">
                  I understand that my medical records and consultation history will be permanently deleted.
                </label>
              </div>
              
              <div class="flex items-start space-x-3">
                <input
                  v-model="form.confirmPermanent"
                  type="checkbox"
                  required
                  class="h-4 w-4 text-red-600 focus:ring-red-500 border-gray-300 rounded mt-1"
                />
                <label class="text-sm text-gray-700">
                  I understand that this action is permanent and cannot be undone.
                </label>
              </div>
            </div>

            <div>
              <label class="block text-sm font-medium text-gray-700 mb-2">
                Type "DELETE" to confirm
              </label>
              <input
                v-model="form.confirmationText"
                type="text"
                required
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-transparent"
                placeholder="Type DELETE to confirm"
                :class="{ 'border-red-500': form.confirmationText && form.confirmationText !== 'DELETE' }"
              />
              <p v-if="form.confirmationText && form.confirmationText !== 'DELETE'" class="text-red-500 text-sm mt-1">
                Please type "DELETE" exactly as shown to confirm.
              </p>
            </div>

            <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4">
              <BaseButton
                type="button"
                @click="$router.push('/account')"
                class="flex-1 px-6 py-3 bg-gray-600 text-white hover:bg-gray-700 transition-all duration-300"
              >
                Cancel
              </BaseButton>
              <BaseButton
                type="submit"
                :disabled="!canDelete || isDeleting"
                class="flex-1 px-6 py-3 bg-red-600 text-white hover:bg-red-700 transition-all duration-300 disabled:opacity-50 disabled:cursor-not-allowed"
              >
                <span v-if="isDeleting" class="flex items-center justify-center">
                  <Icon icon="mdi-loading" class="animate-spin mr-2" :size="20" />
                  Verifying and Deleting Account...
                </span>
                <span v-else>Permanently Delete Account</span>
              </BaseButton>
            </div>
          </form>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import aosMixin from '@/mixins/aos'

export default {
  name: 'DeleteAccountPage',
  mixins: [aosMixin],
  data() {
    return {
      isDeleting: false,
      apiError: '',
      form: {
        email: '',
        password: '',
        reason: '',
        otherReason: '',
        confirmData: false,
        confirmMedical: false,
        confirmPermanent: false,
        confirmationText: ''
      }
    }
  },
  computed: {
    isValidEmail() {
      const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
      return emailRegex.test(this.form.email)
    },
    canDelete() {
      return this.form.email && 
             this.isValidEmail &&
             this.form.password && 
             this.form.confirmData && 
             this.form.confirmMedical && 
             this.form.confirmPermanent && 
             this.form.confirmationText === 'DELETE'
    }
  },
  methods: {
    async confirmDeletion() {
      if (!this.canDelete) return
      
      this.isDeleting = true
      this.apiError = '' // Clear any previous errors
      
      try {
        await this.$fetch('/api/v1/user/account', {
          method: 'DELETE',
          baseURL: 'https://araya-api-a900468737c2.herokuapp.com',
          body: {
            email: this.form.email,
            password: this.form.password,
            reason: this.form.reason,
            otherReason: this.form.otherReason
          }
        })
        
        this.isDeleting = false
        
        // Account successfully deleted
        this.$router.push('/')
        
        // Show success message
        alert('Your account has been permanently deleted. Thank you for using Araya.')
        
      } catch (error) {
        this.isDeleting = false
        
        console.error('Error deleting account:', error)
        
        // Handle different error scenarios
        if (error.response?.status === 401) {
          this.apiError = 'Invalid email or password. Please check your credentials and try again.'
        } else if (error.response?.status === 404) {
          this.apiError = 'Account not found. Please check your email address.'
        } else if (error.response?.status === 400) {
          this.apiError = 'Invalid request. Please check your information and try again.'
        } else {
          this.apiError = 'An error occurred while deleting your account. Please try again later or contact support.'
        }
      }
    }
  }
}
</script>

<style scoped>
/* Custom styles for the delete account page */
</style> 