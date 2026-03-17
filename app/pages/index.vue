<template>
  <div>
    <!-- Additional sections can go here -->
    <section class="py-16 bg-gray-50">
      <div class="container mx-auto px-4">
        <div class="text-center mb-12">
          <h2 class="text-3xl font-bold text-gray-900 mb-4">Our Products & Services</h2>
          <p class="text-lg text-gray-600">Discover our comprehensive range of agricultural and electronic solutions</p>
        </div>
        
        <div class="grid md:grid-cols-3 gap-8">
          <div class="text-center">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <Icon name="i-heroicons-crop" class="w-8 h-8 text-green-600" />
            </div>
            <h3 class="text-xl font-semibold mb-2">Cocoa & Coffee</h3>
            <p class="text-gray-600">Premium quality beans and cocoa products for global markets</p>
          </div>
          <div class="text-center">
            <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <Icon name="i-heroicons-cpu-chip" class="w-8 h-8 text-blue-600" />
            </div>
            <h3 class="text-xl font-semibold mb-2">Electronics</h3>
            <p class="text-gray-600">Cutting-edge electronic components and solutions</p>
          </div>
          <div class="text-center">
            <div class="w-16 h-16 bg-yellow-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <Icon name="i-heroicons-sparkles" class="w-8 h-8 text-yellow-600" />
            </div>
            <h3 class="text-xl font-semibold mb-2">Decor's</h3>
            <p class="text-gray-600">Beautiful decorative items for elegant living spaces</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Agri-Management - Home',
  meta: [
    { name: 'description', content: 'Global trade excellence in agricultural and electronic solutions' }
  ]
})
</script>
