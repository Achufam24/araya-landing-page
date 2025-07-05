<template>
  <div class="col-span-12 lg:col-span-6" v-bind="$attrs">
    <div class="w-full sm:mt-20 xl:mt-0 flex items-center justify-center">
      <div class="relative w-96 h-96">
        <!-- Main platform icon -->
        <div class="w-80 h-80 bg-gradient-to-br from-blue-50 to-blue-100 rounded-full flex items-center justify-center mx-auto">
          <div class="w-64 h-64 bg-white rounded-full flex items-center justify-center shadow-lg">
            <div class="text-center">
              <div class="w-24 h-24 bg-gradient-to-br from-[#1A3E7F] to-[#2B5AA0] rounded-full flex items-center justify-center mx-auto mb-4">
                <Icon icon="mdi-monitor-dashboard" class="text-white" :size="48" />
              </div>
              <h3 class="text-lg font-semibold text-gray-800 mb-2">Telemedicine Platform</h3>
              <p class="text-gray-600 text-sm">Complete healthcare solution</p>
            </div>
          </div>
        </div>
        
        <!-- Feature icons -->
        <div class="absolute -top-4 -left-4 w-16 h-16 bg-green-100 rounded-full flex items-center justify-center">
          <Icon icon="mdi-video" class="text-green-600" :size="24" />
        </div>
        <div class="absolute -bottom-4 -right-4 w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center">
          <Icon icon="mdi-prescription" class="text-purple-600" :size="24" />
        </div>
        <div class="absolute top-1/2 -left-8 w-12 h-12 bg-orange-100 rounded-full flex items-center justify-center">
          <Icon icon="mdi-file-document" class="text-orange-600" :size="20" />
        </div>
        <div class="absolute top-1/2 -right-8 w-12 h-12 bg-red-100 rounded-full flex items-center justify-center">
          <Icon icon="mdi-chart-line" class="text-red-600" :size="20" />
        </div>
      </div>
    </div>
  </div>
</template>
