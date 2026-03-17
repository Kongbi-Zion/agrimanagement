<template>
  <div class="max-w-6xl mx-auto space-y-8 py-8">
    <div class="text-center mb-12">
      <h1 class="text-4xl font-bold text-gray-900 mb-4">Cocoa & Coffee</h1>
      <p class="text-xl text-gray-600">
        Premium quality cocoa and coffee products for global markets
      </p>
    </div>

    <div class="grid md:grid-cols-2 gap-8">
      <section>
        <h2 class="text-2xl font-semibold mb-6">Our Cocoa Products</h2>
        <div class="space-y-4">
          <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
            <h3 class="text-lg font-semibold mb-2">Cocoa Beans</h3>
            <p class="text-gray-600">
              Premium quality cocoa beans sourced from sustainable farms, perfect for chocolate production and industrial applications.
            </p>
          </div>
          <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
            <h3 class="text-lg font-semibold mb-2">Cocoa Butter</h3>
            <p class="text-gray-600">
              High-purity cocoa butter ideal for cosmetics, pharmaceuticals, and confectionery applications.
            </p>
          </div>
          <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
            <h3 class="text-lg font-semibold mb-2">Cocoa Powder</h3>
            <p class="text-gray-600">
              Premium cocoa powder with consistent quality for baking, beverages, and food manufacturing.
            </p>
          </div>
          <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
            <h3 class="text-lg font-semibold mb-2">Cocoa Mass</h3>
            <p class="text-gray-600">
              Pure cocoa mass for chocolate manufacturers and industrial chocolate production.
            </p>
          </div>
        </div>
      </section>

      <section>
        <h2 class="text-2xl font-semibold mb-6">Our Coffee Selection</h2>
        <div class="space-y-4">
          <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
            <h3 class="text-lg font-semibold mb-2">Arabica Beans</h3>
            <p class="text-gray-600">
              Premium Arabica coffee beans with exceptional flavor profiles, sourced from high-altitude farms.
            </p>
          </div>
          <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
            <h3 class="text-lg font-semibold mb-2">Robusta Beans</h3>
            <p class="text-gray-600">
              High-caffeine Robusta beans perfect for espresso blends and instant coffee production.
            </p>
          </div>
          <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
            <h3 class="text-lg font-semibold mb-2">Specialty Blends</h3>
            <p class="text-gray-600">
              Custom coffee blends tailored to specific market requirements and taste preferences.
            </p>
          </div>
        </div>
      </section>
    </div>

    <section class="text-center py-12">
      <h2 class="text-2xl font-semibold mb-6">Why Choose Our Products?</h2>
      <div class="grid md:grid-cols-3 gap-8">
        <div class="text-center">
          <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
            <Icon name="i-heroicons-check-circle" class="w-8 h-8 text-green-600" />
          </div>
          <h3 class="text-lg font-semibold mb-2">Quality Assured</h3>
          <p class="text-gray-600">All products meet international quality standards and certifications.</p>
        </div>
        <div class="text-center">
          <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
            <Icon name="i-heroicons-truck" class="w-8 h-8 text-blue-600" />
          </div>
          <h3 class="text-lg font-semibold mb-2">Global Delivery</h3>
          <p class="text-gray-600">Reliable shipping to destinations worldwide with proper documentation.</p>
        </div>
        <div class="text-center">
          <div class="w-16 h-16 bg-yellow-100 rounded-full flex items-center justify-center mx-auto mb-4">
            <Icon name="i-heroicons-leaf" class="w-8 h-8 text-yellow-600" />
          </div>
          <h3 class="text-lg font-semibold mb-2">Sustainable Sourcing</h3>
          <p class="text-gray-600">Environmentally responsible farming practices and fair trade partnerships.</p>
        </div>
      </div>
    </section>

    <section class="text-center">
      <UButton to="/contact" size="lg" color="primary">
        Contact Us for Inquiries
      </UButton>
    </section>
  </div>
</template>

<script setup>
useHead({
  title: 'Cocoa & Coffee - Agri-Management',
  meta: [
    { name: 'description', content: 'Premium quality cocoa and coffee products for global markets' }
  ]
})
</script>
