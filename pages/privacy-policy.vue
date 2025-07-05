<template>
  <div class="w-full">
    <!-- Hero section -->
    <section class="w-full py-16 bg-gradient-to-br from-blue-50 to-blue-100">
      <div class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
          <span class="text-base text-gradient font-semibold uppercase mb-4">Privacy & Security</span>
          <h1 class="text-4xl sm:text-5xl font-bold text-gray-900 mb-6">
            Privacy <span class="text-header-gradient">Policy</span>
          </h1>
          <p class="text-xl text-gray-600 max-w-3xl mx-auto">
            Your privacy and the security of your health information are our top priorities. Learn how we protect your data.
          </p>
          <div class="mt-8 flex items-center justify-center space-x-6">
            <div class="flex items-center space-x-2">
              <Icon icon="mdi-shield-check" class="text-green-500" :size="20" />
              <span class="text-sm text-gray-600">HIPAA Compliant</span>
            </div>
            <div class="flex items-center space-x-2">
              <Icon icon="mdi-lock" class="text-blue-500" :size="20" />
              <span class="text-sm text-gray-600">256-bit Encryption</span>
            </div>
            <div class="flex items-center space-x-2">
              <Icon icon="mdi-eye-off" class="text-purple-500" :size="20" />
              <span class="text-sm text-gray-600">Data Protected</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Privacy Policy Content -->
    <section class="w-full py-16">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="bg-white rounded-2xl shadow-lg p-8 lg:p-12">
          <div class="prose prose-lg max-w-none">
            <!-- Last Updated -->
            <div class="mb-8 p-4 bg-blue-50 rounded-lg">
              <p class="text-sm text-blue-800">
                <strong>Last Updated:</strong> December 2024
              </p>
            </div>

            <!-- Introduction -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">Introduction</h2>
              <p class="text-gray-700 mb-4">
                Araya ("we," "our," or "us") is committed to protecting your privacy and ensuring the security of your personal health information. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our telemedicine platform and services.
              </p>
              <p class="text-gray-700">
                By using our services, you agree to the collection and use of information in accordance with this policy. We are committed to maintaining the confidentiality of your health information and complying with all applicable privacy laws, including the Health Insurance Portability and Accountability Act (HIPAA).
              </p>
            </div>

            <!-- Information We Collect -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">Information We Collect</h2>
              
              <h3 class="text-xl font-semibold text-gray-800 mb-3">Personal Information</h3>
              <ul class="list-disc pl-6 mb-4 text-gray-700 space-y-2">
                <li>Name, email address, and phone number</li>
                <li>Date of birth and gender</li>
                <li>Emergency contact information</li>
                <li>Insurance information (if applicable)</li>
                <li>Payment and billing information</li>
              </ul>

              <h3 class="text-xl font-semibold text-gray-800 mb-3">Health Information</h3>
              <ul class="list-disc pl-6 mb-4 text-gray-700 space-y-2">
                <li>Medical history and current medications</li>
                <li>Symptoms and health concerns</li>
                <li>Consultation notes and treatment plans</li>
                <li>Prescriptions and medical recommendations</li>
                <li>Lab results and diagnostic information</li>
              </ul>

              <h3 class="text-xl font-semibold text-gray-800 mb-3">Technical Information</h3>
              <ul class="list-disc pl-6 mb-4 text-gray-700 space-y-2">
                <li>Device information and IP address</li>
                <li>Browser type and operating system</li>
                <li>Usage patterns and interaction data</li>
                <li>Cookies and similar tracking technologies</li>
              </ul>
            </div>

            <!-- How We Use Your Information -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">How We Use Your Information</h2>
              <ul class="list-disc pl-6 text-gray-700 space-y-2">
                <li>Provide telemedicine consultations and medical services</li>
                <li>Process payments and manage billing</li>
                <li>Send appointment reminders and notifications</li>
                <li>Improve our services and user experience</li>
                <li>Comply with legal and regulatory requirements</li>
                <li>Protect against fraud and ensure security</li>
                <li>Communicate with you about our services</li>
              </ul>
            </div>

            <!-- Information Sharing -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">Information Sharing and Disclosure</h2>
              <p class="text-gray-700 mb-4">
                We do not sell, trade, or rent your personal information to third parties. We may share your information only in the following circumstances:
              </p>
              
              <h3 class="text-xl font-semibold text-gray-800 mb-3">With Your Consent</h3>
              <p class="text-gray-700 mb-4">
                We may share your information with third parties when you explicitly consent to such sharing.
              </p>

              <h3 class="text-xl font-semibold text-gray-800 mb-3">Healthcare Providers</h3>
              <p class="text-gray-700 mb-4">
                We may share your health information with licensed healthcare providers who are treating you through our platform.
              </p>

              <h3 class="text-xl font-semibold text-gray-800 mb-3">Legal Requirements</h3>
              <p class="text-gray-700 mb-4">
                We may disclose your information when required by law, court order, or government regulation.
              </p>

              <h3 class="text-xl font-semibold text-gray-800 mb-3">Service Providers</h3>
              <p class="text-gray-700 mb-4">
                We may share information with trusted third-party service providers who assist us in operating our platform, such as payment processors and cloud storage providers.
              </p>
            </div>

            <!-- Data Security -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">Data Security</h2>
              <p class="text-gray-700 mb-4">
                We implement comprehensive security measures to protect your personal and health information:
              </p>
              
              <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-4">
                <div class="bg-green-50 p-4 rounded-lg">
                  <h4 class="font-semibold text-green-800 mb-2">Encryption</h4>
                  <p class="text-green-700 text-sm">All data is encrypted using industry-standard 256-bit SSL encryption</p>
                </div>
                <div class="bg-blue-50 p-4 rounded-lg">
                  <h4 class="font-semibold text-blue-800 mb-2">Access Controls</h4>
                  <p class="text-blue-700 text-sm">Strict access controls and authentication protocols</p>
                </div>
                <div class="bg-purple-50 p-4 rounded-lg">
                  <h4 class="font-semibold text-purple-800 mb-2">Regular Audits</h4>
                  <p class="text-purple-700 text-sm">Regular security audits and vulnerability assessments</p>
                </div>
                <div class="bg-orange-50 p-4 rounded-lg">
                  <h4 class="font-semibold text-orange-800 mb-2">HIPAA Compliance</h4>
                  <p class="text-orange-700 text-sm">Full compliance with HIPAA privacy and security rules</p>
                </div>
              </div>
            </div>

            <!-- Your Rights -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">Your Privacy Rights</h2>
              <p class="text-gray-700 mb-4">
                You have the following rights regarding your personal information:
              </p>
              
              <div class="space-y-4">
                <div class="flex items-start space-x-3">
                  <Icon icon="mdi-eye" class="text-blue-500 mt-1" :size="20" />
                  <div>
                    <h4 class="font-semibold text-gray-800">Right to Access</h4>
                    <p class="text-gray-700 text-sm">Request a copy of your personal information</p>
                  </div>
                </div>
                
                <div class="flex items-start space-x-3">
                  <Icon icon="mdi-pencil" class="text-green-500 mt-1" :size="20" />
                  <div>
                    <h4 class="font-semibold text-gray-800">Right to Correct</h4>
                    <p class="text-gray-700 text-sm">Request correction of inaccurate information</p>
                  </div>
                </div>
                
                <div class="flex items-start space-x-3">
                  <Icon icon="mdi-delete" class="text-red-500 mt-1" :size="20" />
                  <div>
                    <h4 class="font-semibold text-gray-800">Right to Delete</h4>
                    <p class="text-gray-700 text-sm">Request deletion of your personal information</p>
                  </div>
                </div>
                
                <div class="flex items-start space-x-3">
                  <Icon icon="mdi-shield-off" class="text-purple-500 mt-1" :size="20" />
                  <div>
                    <h4 class="font-semibold text-gray-800">Right to Opt-Out</h4>
                    <p class="text-gray-700 text-sm">Opt-out of marketing communications</p>
                  </div>
                </div>
              </div>
            </div>

            <!-- Cookies and Tracking -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">Cookies and Tracking Technologies</h2>
              <p class="text-gray-700 mb-4">
                We use cookies and similar technologies to enhance your experience on our platform:
              </p>
              
              <h3 class="text-xl font-semibold text-gray-800 mb-3">Essential Cookies</h3>
              <p class="text-gray-700 mb-4">
                These cookies are necessary for the platform to function properly and cannot be disabled.
              </p>
              
              <h3 class="text-xl font-semibold text-gray-800 mb-3">Analytics Cookies</h3>
              <p class="text-gray-700 mb-4">
                These cookies help us understand how users interact with our platform to improve our services.
              </p>
              
              <h3 class="text-xl font-semibold text-gray-800 mb-3">Marketing Cookies</h3>
              <p class="text-gray-700 mb-4">
                These cookies are used to deliver relevant advertisements and track marketing campaign performance.
              </p>
            </div>

            <!-- Children's Privacy -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">Children's Privacy</h2>
              <p class="text-gray-700 mb-4">
                Our services are not intended for children under the age of 13. We do not knowingly collect personal information from children under 13. If you are a parent or guardian and believe your child has provided us with personal information, please contact us immediately.
              </p>
            </div>

            <!-- International Users -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">International Users</h2>
              <p class="text-gray-700 mb-4">
                If you are accessing our services from outside the United States, please be aware that your information may be transferred to, stored, and processed in the United States where our servers are located. By using our services, you consent to the transfer of your information to the United States.
              </p>
            </div>

            <!-- Changes to Privacy Policy -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">Changes to This Privacy Policy</h2>
              <p class="text-gray-700 mb-4">
                We may update this Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page and updating the "Last Updated" date. We encourage you to review this Privacy Policy periodically for any changes.
              </p>
            </div>

            <!-- Contact Information -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">Contact Us</h2>
              <p class="text-gray-700 mb-4">
                If you have any questions about this Privacy Policy or our privacy practices, please contact us:
              </p>
              
              <div class="bg-gray-50 p-6 rounded-lg">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                  <div>
                    <h4 class="font-semibold text-gray-800 mb-2">Email</h4>
                    <p class="text-gray-700">admin@araya.com</p>
                  </div>
                  <div>
                    <h4 class="font-semibold text-gray-800 mb-2">Phone</h4>
                    <p class="text-gray-700">+2347062881214</p>
                  </div>
                  <div>
                    <h4 class="font-semibold text-gray-800 mb-2">Address</h4>
                    <p class="text-gray-700">
                      Araya Health<br>
                      Lagos, Nigeria<br>
                      Suite 100<br>
                      Lagos, Nigeria
                    </p>
                  </div>
                  <div>
                    <h4 class="font-semibold text-gray-800 mb-2">Privacy Officer</h4>
                    <p class="text-gray-700">admin@araya.com</p>
                  </div>
                </div>
              </div>
            </div>

            <!-- Additional Resources -->
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-gray-900 mb-4">Additional Resources</h2>
              <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="bg-blue-50 p-4 rounded-lg">
                  <h4 class="font-semibold text-blue-800 mb-2">Terms of Service</h4>
                  <p class="text-blue-700 text-sm mb-3">Read our terms of service and user agreement</p>
                  <BaseButton class="px-4 py-2 bg-blue-600 text-white text-sm hover:bg-blue-700 transition-all duration-300">
                    View Terms
                  </BaseButton>
                </div>
                <div class="bg-green-50 p-4 rounded-lg">
                  <h4 class="font-semibold text-green-800 mb-2">HIPAA Notice</h4>
                  <p class="text-green-700 text-sm mb-3">Learn about your HIPAA rights and our practices</p>
                  <BaseButton class="px-4 py-2 bg-green-600 text-white text-sm hover:bg-green-700 transition-all duration-300">
                    HIPAA Notice
                  </BaseButton>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Trust Indicators -->
    <section class="w-full py-16 bg-gray-50">
      <div class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-12">
          <h2 class="text-3xl font-bold text-gray-900 mb-4">Your Privacy is Our Priority</h2>
          <p class="text-gray-600 max-w-2xl mx-auto">
            We're committed to maintaining the highest standards of privacy and security for your health information.
          </p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="text-center">
            <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <Icon icon="mdi-shield-check" class="text-blue-600" :size="32" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">HIPAA Compliant</h3>
            <p class="text-gray-600">
              Full compliance with federal health privacy regulations
            </p>
          </div>
          
          <div class="text-center">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <Icon icon="mdi-lock" class="text-green-600" :size="32" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Bank-Level Security</h3>
            <p class="text-gray-600">
              Enterprise-grade encryption and security protocols
            </p>
          </div>
          
          <div class="text-center">
            <div class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <Icon icon="mdi-eye-off" class="text-purple-600" :size="32" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Your Control</h3>
            <p class="text-gray-600">
              Complete control over your data and privacy settings
            </p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'PrivacyPolicy',
  head() {
    return {
      title: 'Privacy Policy - Araya Health',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Learn about Araya Health\'s privacy policy and how we protect your personal and health information. HIPAA compliant telemedicine platform.'
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content: 'privacy policy, HIPAA, telemedicine, health privacy, data protection, medical privacy'
        }
      ]
    }
  }
}
</script>

<style scoped>
.prose h2 {
  @apply text-2xl font-bold text-gray-900 mb-4;
}

.prose h3 {
  @apply text-xl font-semibold text-gray-800 mb-3;
}

.prose h4 {
  @apply font-semibold text-gray-800 mb-2;
}

.prose p {
  @apply text-gray-700 mb-4;
}

.prose ul {
  @apply list-disc pl-6 text-gray-700 space-y-2;
}

.prose li {
  @apply text-gray-700;
}
</style> 