<template>
  <div class="w-full">
    <!-- Hero section -->
    <section id="hero" class="w-full pb-24">
      <BaseSection>
        <div class="col-span-12 lg:col-span-6 mt-12 xl:mt-10 space-y-4 sm:space-y-6 px-6 text-center sm:text-left">
          <span data-aos="fade-right" data-aos-once="true" class="text-base text-gradient font-semibold uppercase"
            >24/7 Healthcare Access</span
          >
          <h1
            data-aos="fade-right"
            data-aos-once="true"
            class="text-[2.5rem] sm:text-5xl xl:text-6xl font-bold leading-tight capitalize sm:pr-8 xl:pr-10"
          >
            Connect with <span class="text-header-gradient">Board-Certified</span> Doctors Instantly
          </h1>
          <p data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="paragraph hidden sm:block">
            Get expert medical care from the comfort of your home. Video consultations, prescriptions, and health advice from licensed physicians in under 5 minutes.
          </p>
          <div
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-delay="700"
            class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4 mt-2"
          >
            <BaseButton
              class="max-w-full px-8 py-4 bg-gradient-to-r from-[#1A3E7F] to-[#2B5AA0] border border-[#1A3E7F] text-white hover:shadow-lg transition-all duration-300"
            >
              Start Free Consultation
            </BaseButton>
            <div class="flex flex-col sm:flex-row space-y-2 sm:space-y-0 sm:space-x-2">
              <BaseButton
                class="max-w-full px-6 py-4 bg-black text-white border border-black flex items-center justify-center hover:bg-gray-800 transition-all duration-300"
              >
                <span class="flex items-center">
                  <Icon icon="mdi-apple" class="mr-2" :size="20" />
                  Download on App Store
                </span>
              </BaseButton>
              <BaseButton
                class="max-w-full px-6 py-4 bg-black text-white border border-black flex items-center justify-center hover:bg-gray-800 transition-all duration-300"
              >
                <span class="flex items-center">
                  <Icon icon="mdi-google-play" class="mr-2" :size="20" />
                  Get it on Google Play
                </span>
              </BaseButton>
            </div>
          </div>
          <div data-aos="fade-up" data-aos-delay="900" class="flex items-center space-x-6 pt-4">
            <div class="flex items-center space-x-2">
              <Icon icon="mdi-check-circle" class="text-green-500" :size="20" />
              <span class="text-sm text-gray-600">HIPAA Compliant</span>
            </div>
            <div class="flex items-center space-x-2">
              <Icon icon="mdi-clock" class="text-blue-500" :size="20" />
              <span class="text-sm text-gray-600">24/7 Available</span>
            </div>
            <div class="flex items-center space-x-2">
              <Icon icon="mdi-shield-check" class="text-purple-500" :size="20" />
              <span class="text-sm text-gray-600">Licensed Doctors</span>
            </div>
          </div>
        </div>
        <div class="hidden sm:block col-span-12 lg:col-span-6">
          <div class="w-full flex items-center justify-center">
            <div class="relative">
              <!-- Main telemedicine icon -->
              <div class="w-96 h-96 bg-gradient-to-br from-blue-50 to-blue-100 rounded-full flex items-center justify-center">
                <div class="w-80 h-80 bg-white rounded-full flex items-center justify-center shadow-lg">
                  <div class="text-center">
                    <div class="w-32 h-32 bg-gradient-to-br from-[#1A3E7F] to-[#2B5AA0] rounded-full flex items-center justify-center mx-auto mb-6">
                      <Icon icon="mdi-doctor" class="text-white" :size="64" />
                    </div>
                    <h3 class="text-xl font-semibold text-gray-800 mb-2">24/7 Medical Care</h3>
                    <p class="text-gray-600 text-sm">Connect with licensed doctors instantly</p>
                  </div>
                </div>
              </div>
              
              <!-- Floating elements -->
              <div class="absolute -top-4 -right-4 w-16 h-16 bg-green-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-video" class="text-green-600" :size="24" />
              </div>
              <div class="absolute -bottom-4 -left-4 w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-prescription" class="text-purple-600" :size="24" />
              </div>
              <div class="absolute top-1/2 -right-8 w-12 h-12 bg-orange-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-clock" class="text-orange-600" :size="20" />
              </div>
            </div>
          </div>
        </div>
        
        <!-- Decorative elements with icons -->
        <div class="hidden sm:block absolute bottom-12 xl:bottom-16 left-4 xl:left-0">
          <div class="w-8 h-8 bg-blue-100 rounded-full flex items-center justify-center">
            <Icon icon="mdi-heart-pulse" class="text-blue-600" :size="16" />
          </div>
        </div>
        <div class="hidden sm:block absolute top-4 sm:top-10 right-64 sm:right-96 xl:right-[32rem]">
          <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center">
            <Icon icon="mdi-shield-check" class="text-green-600" :size="16" />
          </div>
        </div>
        <div class="hidden sm:block absolute bottom-56 right-24">
          <div class="w-8 h-8 bg-purple-100 rounded-full flex items-center justify-center">
            <Icon icon="mdi-stethoscope" class="text-purple-600" :size="16" />
          </div>
        </div>
        <div class="hidden sm:block absolute top-20 sm:top-28 right-16 lg:right-0 lg:left-[30rem]">
          <div class="w-10 h-10 bg-orange-100 rounded-full flex items-center justify-center">
            <Icon icon="mdi-star" class="text-orange-600" :size="20" />
          </div>
        </div>
      </BaseSection>
    </section>

    <!-- Medical statistics section -->
    <section
      class="max-w-screen-xl mx-2 sm:mx-auto px-4 sm:px-6 lg:px-0 py-6 pb-20 sm:py-8 rounded-[2.25rem] sm:rounded-xl bg-white shadow-lg sm:shadow-md transform lg:-translate-y-12"
    >
      <div class="w-full flex flex-col lg:flex-row items-center justify-center">
        <LandingSimpleStatistic
          data-aos="fade-up"
          title="🏥 Active Doctors"
          subtitle="Licensed healthcare providers"
          :stats="activeDoctorsStats"
          class="xl:border-r border-gray-200 lg:px-8"
        />
        <LandingSimpleStatistic
          data-aos="fade-up"
          data-aos-delay="150"
          title="👥 Patients Served"
          subtitle="Happy patients worldwide"
          :stats="patientsStats"
          class="xl:border-r border-gray-200 lg:px-8"
        />
        <LandingSimpleStatistic
          data-aos="fade-up"
          data-aos-delay="300"
          title="⭐ Satisfaction Rate"
          subtitle="Patient satisfaction score"
          :stats="satisfactionStats"
          class="lg:px-8"
        />
      </div>
    </section>

    <!-- Book consultation section -->
    <section class="w-full my-24">
      <BaseSection>
        <LandingBuyTradeImage class="sm:hidden mb-8" />
        <div data-aos="fade-right" class="col-span-12 lg:col-span-6 mt-4 xl:mt-20 space-y-6 px-4">
          <span class="text-base text-gradient font-semibold uppercase">Quick Booking</span>
          <h2 class="text-4xl font-semibold sm:pr-8 xl:pr-12">
            See a doctor in <br class="hidden sm:block" />
            <span class="text-header-gradient">under 5 minutes</span>
          </h2>
          <p class="paragraph">
            No waiting rooms, no travel time. Connect with board-certified physicians instantly for urgent care, prescriptions, and health consultations.
          </p>
          <div class="space-y-6 lg:pr-12">
            <div class="bg-gray-50 p-4 rounded-lg">
              <h4 class="font-medium text-gray-800 mb-2">What we treat:</h4>
              <div class="grid grid-cols-2 gap-2 text-sm">
                <div class="flex items-center space-x-2">
                  <Icon icon="mdi-check" class="text-green-500" :size="16" />
                  <span>Cold & Flu</span>
                </div>
                <div class="flex items-center space-x-2">
                  <Icon icon="mdi-check" class="text-green-500" :size="16" />
                  <span>Skin Conditions</span>
                </div>
                <div class="flex items-center space-x-2">
                  <Icon icon="mdi-check" class="text-green-500" :size="16" />
                  <span>Mental Health</span>
                </div>
                <div class="flex items-center space-x-2">
                  <Icon icon="mdi-check" class="text-green-500" :size="16" />
                  <span>Prescriptions</span>
                </div>
              </div>
            </div>
            <LandingExchange
              title="Consultation Type"
              name="consultation"
              type="text"
              default-value="General Health"
              :exchange-selected="consultationSelected"
              :exchanges="consultationTypes"
            />
            <LandingExchange
              title="Duration"
              name="duration"
              type="text"
              default-value="15 minutes"
              :exchange-selected="durationSelected"
              :exchanges="durations"
            />
            <BaseButton class="w-full px-5 py-4 bg-gradient-to-r from-[#1A3E7F] to-[#2B5AA0] text-white text-base font-medium hover:shadow-lg transition-all duration-300">
              <span class="flex items-center justify-center">
                <Icon icon="mdi-video" class="mr-2" :size="20" />
                Start Video Consultation
              </span>
            </BaseButton>
          </div>
        </div>
        <LandingBuyTradeImage data-aos="fade-left" class="hidden sm:block" />
      </BaseSection>
    </section>

    <!-- Healthcare partners section -->
    <section class="bg-partner relative max-w-full sm:mx-6 my-24 shadow sm:rounded-2xl overflow-hidden">
      <div class="w-full px-6 sm:px-0 py-16 flex flex-col items-center justify-center space-y-4 text-center">
        <h3 data-aos="flip-down" class="text-2xl text-neutral-800 font-semibold">Trusted Healthcare Partners</h3>
        <p data-aos="flip-down" class="paragraph">We partner with leading hospitals and medical institutions worldwide</p>
        <div data-aos="fade-up" class="flex flex-wrap items-center justify-center">
          <LandingPartnerImage
            v-for="img in ['clever.png', 'diamon-cutts.png', 'swiss-finance.png', 'gambio.png']"
            :key="img"
            :img="img"
          />
        </div>
      </div>
    </section>

    <!-- Health card section -->
    <section class="w-full my-36">
      <BaseSection data-aos="fade-down">
        <div class="col-span-12 lg:col-span-7">
          <div class="w-full flex items-center justify-center">
            <div class="relative w-96 h-64 bg-gradient-to-br from-[#1A3E7F] to-[#2B5AA0] rounded-2xl shadow-xl p-6">
              <!-- Card design -->
              <div class="absolute inset-0 bg-white rounded-2xl transform rotate-3 translate-x-2 translate-y-2"></div>
              <div class="relative bg-gradient-to-br from-[#1A3E7F] to-[#2B5AA0] rounded-2xl p-6 text-white">
                <div class="flex justify-between items-start mb-8">
                  <div>
                    <h3 class="text-2xl font-bold">Araya Health</h3>
                    <p class="text-blue-100">Digital Health Card</p>
                  </div>
                  <div class="w-12 h-12 bg-white bg-opacity-20 rounded-full flex items-center justify-center">
                    <Icon icon="mdi-heart-pulse" class="text-white" :size="24" />
                  </div>
                </div>
                
                <div class="space-y-4">
                  <div class="flex items-center space-x-3">
                    <Icon icon="mdi-shield-check" class="text-green-300" :size="20" />
                    <span class="text-sm">HIPAA Compliant</span>
                  </div>
                  <div class="flex items-center space-x-3">
                    <Icon icon="mdi-prescription" class="text-blue-300" :size="20" />
                    <span class="text-sm">Digital Prescriptions</span>
                  </div>
                  <div class="flex items-center space-x-3">
                    <Icon icon="mdi-clock" class="text-yellow-300" :size="20" />
                    <span class="text-sm">24/7 Access</span>
                  </div>
                </div>
                
                <div class="mt-6 flex justify-between items-center">
                  <div class="text-xs text-blue-100">
                    <div>Card Number</div>
                    <div class="font-mono">**** **** **** 1234</div>
                  </div>
                  <div class="text-xs text-blue-100">
                    <div>Valid Thru</div>
                    <div>12/25</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-span-12 lg:col-span-5 space-y-6 px-4 sm:px-6 mt-20">
          <h2 class="text-4xl font-semibold">
            Introducing the <span class="text-header-gradient">Araya</span> Health Card
          </h2>
          <p class="paragraph">Your digital health passport for seamless medical care and insurance coverage.</p>
          <ul class="space-y-4 sm:space-y-2">
            <LandingListItem title="Instant insurance verification" />
            <LandingListItem title="Digital prescription management" />
            <LandingListItem title="No annual fee" />
          </ul>
          <BaseButton
            class="w-full sm:max-w-[240px] px-10 py-4 bg-inherit text-gradient border border-[#1A3E7F] text-base"
            >Join the waitlist</BaseButton
          >
        </div>
      </BaseSection>
    </section>

    <!-- Advanced healthcare features section -->
    <section class="bg-trading-tools relative max-w-full sm:mx-4 my-20 py-16 shadow rounded-2xl overflow-hidden">
      <div class="relative max-w-screen-xl px-4 sm:px-2 mx-auto grid grid-cols-12 gap-x-6">
        <LandingTradingToolImage class="sm:hidden" />
        <div data-aos="fade-right" class="col-span-12 lg:col-span-6 space-y-8 sm:space-y-6 px-4 sm:px-6 mt-8">
          <span class="text-base text-gradient font-semibold uppercase">Platform Features</span>
          <h2 class="text-4xl font-semibold">Complete <span class="text-header-gradient">Telemedicine</span> Solution</h2>
          <div class="space-y-6">
            <div class="flex items-start space-x-4">
              <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center flex-shrink-0">
                <Icon icon="mdi-video" class="text-blue-600" :size="24" />
              </div>
              <div>
                <h4 class="text-lg font-medium">HD Video Consultations</h4>
                <p class="paragraph text-sm xl:text-base">
                  Crystal clear video calls with board-certified doctors. No downloads required - works directly in your browser or mobile app.
                </p>
              </div>
            </div>
            <div class="flex items-start space-x-4">
              <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center flex-shrink-0">
                <Icon icon="mdi-prescription" class="text-green-600" :size="24" />
              </div>
              <div>
                <h4 class="text-lg font-medium">Digital Prescriptions</h4>
                <p class="paragraph text-sm xl:text-base">
                  Get prescriptions sent directly to your preferred pharmacy. Instant refills and medication management all in one place.
                </p>
              </div>
            </div>
            <div class="flex items-start space-x-4">
              <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center flex-shrink-0">
                <Icon icon="mdi-file-document" class="text-purple-600" :size="24" />
              </div>
              <div>
                <h4 class="text-lg font-medium">Health Records</h4>
                <p class="paragraph text-sm xl:text-base">
                  Secure digital health records with easy sharing capabilities. Keep track of your medical history and treatment plans.
                </p>
              </div>
            </div>
          </div>
          <div class="flex flex-col sm:flex-row space-y-3 sm:space-y-0 sm:space-x-4">
            <BaseButton class="px-8 py-4 bg-gradient-to-r from-[#1A3E7F] to-[#2B5AA0] text-white border border-[#1A3E7F] text-base hover:shadow-lg transition-all duration-300">
              Try Free Consultation
            </BaseButton>
            <BaseButton class="bg-inherit text-[#1A3E7F] px-8 py-4 text-center underline rounded-full hover:bg-blue-50 transition-all duration-300">
              View All Features
            </BaseButton>
          </div>
        </div>
        <LandingTradingToolImage data-aos="fade-left" class="hidden sm:block" />
      </div>
    </section>

    <!-- Healthcare security section -->
    <section class="w-full my-24">
      <div class="relative max-w-screen-xl px-8 mx-auto grid grid-cols-12 gap-x-6">
        <div data-aos="fade-right" class="col-span-12 lg:col-span-6">
          <div class="w-full flex items-center justify-center">
            <div class="relative w-96 h-96">
              <!-- Main security icon -->
              <div class="w-80 h-80 bg-gradient-to-br from-blue-50 to-blue-100 rounded-full flex items-center justify-center mx-auto">
                <div class="w-64 h-64 bg-white rounded-full flex items-center justify-center shadow-lg">
                  <div class="text-center">
                    <div class="w-24 h-24 bg-gradient-to-br from-[#1A3E7F] to-[#2B5AA0] rounded-full flex items-center justify-center mx-auto mb-4">
                      <Icon icon="mdi-shield-lock" class="text-white" :size="48" />
                    </div>
                    <h3 class="text-lg font-semibold text-gray-800 mb-2">HIPAA Compliant</h3>
                    <p class="text-gray-600 text-sm">Your health data is secure</p>
                  </div>
                </div>
              </div>
              
              <!-- Security elements -->
              <div class="absolute -top-4 -left-4 w-16 h-16 bg-green-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-lock" class="text-green-600" :size="24" />
              </div>
              <div class="absolute -bottom-4 -right-4 w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-encryption" class="text-purple-600" :size="24" />
              </div>
              <div class="absolute top-1/2 -left-8 w-12 h-12 bg-orange-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-certificate" class="text-orange-600" :size="20" />
              </div>
              <div class="absolute top-1/2 -right-8 w-12 h-12 bg-red-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-security" class="text-red-600" :size="20" />
              </div>
            </div>
          </div>
        </div>
        <div data-aos="fade-left" class="col-span-12 lg:col-span-5 space-y-8 sm:space-y-6 mt-8 xl:px-8">
          <h2 class="text-4xl font-semibold">HIPAA-compliant security from day one</h2>
          <ul class="space-y-8 sm:space-y-4">
            <LandingListItem title="Patient privacy and data protection">
              <p class="text-sm text-gray-700 leading-relaxed">
                Araya is a HIPAA-compliant platform that undergoes regular security audits and is subject to the
                strictest healthcare data protection standards.
                <span class="underline">Learn more</span> about our commitment to patient privacy.
              </p>
            </LandingListItem>
            <LandingListItem title="End-to-end encryption">
              <p class="text-sm text-gray-700 leading-relaxed">
                With Araya you can secure your health data with military-grade encryption and secure authentication.
              </p>
            </LandingListItem>
            <LandingListItem title="SOC 2 & HIPAA Certifications">
              <p class="text-sm text-gray-700 leading-relaxed">
                Araya is <span class="underline">SOC 2 Type 2</span> and
                <span class="underline">HIPAA</span> compliant. We are among the first telemedicine platforms
                to achieve these rigorous security standards.
              </p>
            </LandingListItem>
          </ul>
        </div>
      </div>
    </section>

    <!-- Getting started section -->
    <section class="bg-trading-tools relative max-w-full sm:mx-4 xl:mx-10 my-24 shadow sm:rounded-2xl overflow-hidden">
      <div class="w-full py-16 flex flex-col items-center">
        <span class="text-base text-gradient font-semibold uppercase mb-2">Simple Process</span>
        <h2 data-aos="flip-down" class="text-3xl sm:text-4xl font-semibold text-center">
          Get care in 3 easy steps
        </h2>
        <p data-aos="flip-down" data-aos-delay="150" class="paragraph text-center max-w-2xl mt-4">
          From signup to consultation, our streamlined process gets you connected with healthcare providers faster than ever.
        </p>
        <div
          data-aos="fade-up"
          class="relative w-full flex flex-col lg:flex-row items-center justify-between space-y-12 lg:space-y-0 px-4 xl:px-10 mt-16 sm:mt-8"
        >
          <LandingStep v-for="step in steps" :key="step.title" :step="step" />
          <div class="hidden lg:flex absolute top-32 left-64 xl:left-[22rem] w-24 xl:w-[9.5rem] items-center justify-center">
            <Icon icon="mdi-arrow-right" class="text-[#1A3E7F]" :size="40" />
          </div>
          <div class="hidden lg:flex absolute top-32 right-64 xl:right-[22rem] w-24 xl:w-[9.5rem] items-center justify-center">
            <Icon icon="mdi-arrow-right" class="text-[#1A3E7F]" :size="40" />
          </div>
        </div>
        <div data-aos="fade-up" data-aos-delay="300" class="mt-12 text-center">
          <BaseButton class="px-8 py-4 bg-gradient-to-r from-[#1A3E7F] to-[#2B5AA0] text-white hover:shadow-lg transition-all duration-300">
            Start Your Free Consultation
          </BaseButton>
        </div>
      </div>
    </section>

    <!-- FAQ section -->
    <section class="w-full my-24">
      <BaseSection>
        <div data-aos="fade-right" data-aos-delay="150" class="col-span-12 lg:col-span-6">
          <div class="w-full flex items-center justify-center">
            <div class="relative w-96 h-96">
              <!-- Main support icon -->
              <div class="w-80 h-80 bg-gradient-to-br from-blue-50 to-blue-100 rounded-full flex items-center justify-center mx-auto">
                <div class="w-64 h-64 bg-white rounded-full flex items-center justify-center shadow-lg">
                  <div class="text-center">
                    <div class="w-24 h-24 bg-gradient-to-br from-[#1A3E7F] to-[#2B5AA0] rounded-full flex items-center justify-center mx-auto mb-4">
                      <Icon icon="mdi-headset" class="text-white" :size="48" />
                    </div>
                    <h3 class="text-lg font-semibold text-gray-800 mb-2">24/7 Support</h3>
                    <p class="text-gray-600 text-sm">We're here to help you</p>
                  </div>
                </div>
              </div>
              
              <!-- Support elements -->
              <div class="absolute -top-4 -left-4 w-16 h-16 bg-green-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-chat" class="text-green-600" :size="24" />
              </div>
              <div class="absolute -bottom-4 -right-4 w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-phone" class="text-purple-600" :size="24" />
              </div>
              <div class="absolute top-1/2 -left-8 w-12 h-12 bg-orange-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-email" class="text-orange-600" :size="20" />
              </div>
              <div class="absolute top-1/2 -right-8 w-12 h-12 bg-red-100 rounded-full flex items-center justify-center">
                <Icon icon="mdi-help-circle" class="text-red-600" :size="20" />
              </div>
            </div>
          </div>
        </div>
        <div data-aos="fade-left" data-aos-delay="150" class="col-span-12 lg:col-span-6 px-4 sm:px-6 mt-8">
          <span class="text-base text-gradient font-semibold uppercase mb-4 sm:mb-2">Patient Support</span>
          <h2 class="text-3xl sm:text-4xl font-semibold mb-6">Common questions about telemedicine</h2>
          <p class="paragraph mb-8">Everything you need to know about getting care through Araya's telemedicine platform.</p>

          <ul class="shadow-box">
            <BaseAccordion v-for="(accordion, index) in accordions" :key="index" :accordion="accordion" />
          </ul>
          
          <div class="mt-8 p-6 bg-blue-50 rounded-lg">
            <h4 class="font-medium text-gray-800 mb-2 flex items-center">
              <Icon icon="mdi-headset" class="mr-2 text-blue-600" :size="20" />
              Need more help?
            </h4>
            <p class="text-sm text-gray-600 mb-3">Our support team is available 24/7 to answer your questions.</p>
            <BaseButton class="px-6 py-2 bg-[#1A3E7F] text-white text-sm hover:bg-[#2B5AA0] transition-all duration-300">
              Contact Support
            </BaseButton>
          </div>
        </div>
      </BaseSection>
    </section>

    <div class="w-full my-10 flex justify-center">
      <a
        v-smooth-scroll
        data-aos="flip-down"
        data-aos-delay="150"
        href="#navbar"
        class="px-6 py-3 flex items-center space-x-2 bg-[#FAFAFA] hover:bg-gray-100 hover:shadow-md border border-[#DDDDDD] rounded-md text-gray-700"
      >
        <span>Back to top</span>
        <ArrowUpIcon :size="20" />
      </a>
    </div>
  </div>
</template>

<script>
import aosMixin from '@/mixins/aos'
export default {
  name: 'IndexPage',
  mixins: [aosMixin],
  data() {
    return {
      selected: 0,
      dropdownConcurency: false,
      dropdownCrypto: false,
      currencySelected: {
        img: 'country-icon/eng.png',
        name: 'USD',
      },
      currencies: [
        {
          img: 'country-icon/eng.png',
          name: 'USD',
        },
      ],
      cryptoSelected: {
        img: 'crypto-icon/bitcoin.png',
        name: 'BTC',
      },
      cryptocurrencies: [
        {
          img: 'crypto-icon/bitcoin.png',
          name: 'BTC',
        },
      ],
      activeDoctorsStats: [
        {
          id: 1,
          value: 2500,
          label: 'Total Doctors',
          icon: 'mdi-doctor',
          increase: true,
          change: '+12% this month',
        },
        {
          id: 2,
          value: 150,
          label: 'New This Month',
          icon: 'mdi-plus-circle',
          increase: true,
          change: '+8% from last month',
        },
        {
          id: 3,
          value: 24,
          label: 'Average Response Time (hrs)',
          icon: 'mdi-clock',
          increase: false,
          change: '-2hrs from last month',
        },
      ],
      patientsStats: [
        {
          id: 1,
          value: 125000,
          label: 'Total Patients',
          icon: 'mdi-account-group',
          increase: true,
          change: '+15% this month',
        },
        {
          id: 2,
          value: 89000,
          label: 'Active Users',
          icon: 'mdi-account-check',
          increase: true,
          change: '+22% this month',
        },
        {
          id: 3,
          value: 67000,
          label: 'Consultations This Month',
          icon: 'mdi-video',
          increase: true,
          change: '+18% from last month',
        },
      ],
      satisfactionStats: [
        {
          id: 1,
          value: 98,
          label: 'Patient Satisfaction (%)',
          icon: 'mdi-star',
          increase: true,
          change: '+2% this month',
        },
        {
          id: 2,
          value: 4.9,
          label: 'Average Doctor Rating',
          icon: 'mdi-star-outline',
          increase: true,
          change: '+0.1 from last month',
        },
        {
          id: 3,
          value: 96,
          label: 'Success Rate (%)',
          icon: 'mdi-check-circle',
          increase: true,
          change: '+1% this month',
        },
      ],
      accordions: [
        {
          title: 'How does Araya telemedicine work?',
          description:
            "Araya connects you with licensed healthcare providers through secure video consultations. Simply download our app, create an account, select your health concern, and get connected with a board-certified doctor within minutes. Our platform supports consultations for general health, pediatrics, mental health, dermatology, and more.",
        },
        {
          title: 'Are the doctors on Araya licensed and qualified?',
          description:
            "Yes, all doctors on Araya are board-certified, licensed healthcare providers who have undergone rigorous credentialing. We verify each provider's medical license, board certifications, and malpractice history. Our doctors have an average of 15+ years of clinical experience and are available 24/7.",
        },
        {
          title: 'What health conditions can be treated through Araya?',
          description:
            "Araya can treat a wide range of non-emergency conditions including cold and flu symptoms, skin conditions, mental health concerns, prescription refills, chronic disease management, and preventive care. For emergencies, please call 911 or visit the nearest emergency room immediately.",
        },
        {
          title: 'How much does a consultation cost?',
          description:
            "Consultation costs vary by type and duration, typically ranging from $25 for a 15-minute general consultation to $75 for specialized care. We accept most major insurance plans and offer affordable self-pay options. Check our pricing page for detailed information about your specific insurance coverage.",
        },
        {
          title: 'Is my health information secure on Araya?',
          description:
            "Absolutely. Araya is HIPAA-compliant and uses military-grade encryption to protect your health data. We never share your information with third parties without your explicit consent. All consultations are confidential and your medical records are stored securely in our encrypted database.",
        },
        {
          title: 'Can I get prescriptions through Araya?',
          description:
            "Yes, our licensed providers can prescribe medications when medically appropriate. This includes antibiotics, chronic disease medications, mental health medications, and more. Prescriptions are sent directly to your preferred pharmacy for convenient pickup or delivery.",
        },
      ],
      steps: [
        {
          img: 'sign-up.png',
          title: 'Sign Up',
          description:
            'Create your Araya account on web, iOS or Android and complete your health profile with medical history and insurance information',
        },
        {
          img: 'fund.png',
          title: 'Select Care',
          description:
            'Choose your consultation type, preferred doctor, and appointment time that works best for your schedule',
        },
        {
          img: 'buy-crypto.png',
          title: 'Get Care',
          description:
            'Connect with your doctor via secure video call, receive diagnosis and treatment, and get prescriptions sent to your pharmacy',
        },
      ],
      consultationSelected: {
        img: 'getting-started/sign-up.png',
        name: 'General Health',
      },
      consultationTypes: [
        {
          img: 'getting-started/sign-up.png',
          name: 'General Health',
        },
        {
          img: 'getting-started/fund.png',
          name: 'Pediatrics',
        },
        {
          img: 'getting-started/buy-crypto.png',
          name: 'Mental Health',
        },
        {
          img: 'getting-started/fund.png',
          name: 'Dermatology',
        },
      ],
      durationSelected: {
        img: 'getting-started/arrow.png',
        name: '15 minutes',
      },
      durations: [
        {
          img: 'getting-started/arrow.png',
          name: '15 minutes',
        },
        {
          img: 'getting-started/arrow.png',
          name: '30 minutes',
        },
        {
          img: 'getting-started/arrow.png',
          name: '1 hour',
        },
      ],
    }
  },
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

.bg-partner {
  background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
  background-size: cover;
  background-position: center;
}

.bg-trading-tools {
  background: linear-gradient(135deg, #1A3E7F 0%, #2B5AA0 100%);
  background-size: cover;
  background-position: center;
}

.max-h-0 {
  max-height: 0;
}

/* Telemedicine specific styles */
.telemedicine-card {
  background: white;
  border-radius: 16px;
  box-shadow: 0 4px 20px rgba(26, 62, 127, 0.1);
  transition: all 0.3s ease;
}

.telemedicine-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 30px rgba(26, 62, 127, 0.15);
}

.health-gradient {
  background: linear-gradient(135deg, #1A3E7F 0%, #2B5AA0 50%, #4A8FF6 100%);
}

.emergency-red {
  color: #dc2626;
}

.success-green {
  color: #059669;
}

.warning-orange {
  color: #ea580c;
}
</style>
