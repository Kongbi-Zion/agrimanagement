<template>
  <div class="min-h-screen bg-gray-50">

    <div class="container mx-auto px-4 py-16">
      <div class="max-w-4xl mx-auto">
        <div class="space-y-12">
          <!-- Company Overview -->
          <div class="text-center space-y-6">
            <h2 class="text-3xl md:text-4xl font-semibold text-gray-900">
              Our Story
            </h2>
            <p class="text-lg text-gray-600 leading-relaxed">
              Agri-Management is a leading export-import company specializing in Cameroon's finest agricultural products. We bridge the gap between local farmers and international markets, ensuring quality and sustainability in every transaction.
            </p>
          </div>

          <!-- Mission & Vision -->
          <div class="grid md:grid-cols-2 gap-8">
            <div class="bg-white p-8 rounded-xl shadow-sm">
              <h3 class="text-2xl font-semibold text-gray-900 mb-4">Our Mission</h3>
              <p class="text-gray-600 leading-relaxed">
                To deliver premium quality agricultural products from Cameroon to the global market while supporting local farmers and promoting sustainable farming practices.
              </p>
            </div>
            <div class="bg-white p-8 rounded-xl shadow-sm">
              <h3 class="text-2xl font-semibold text-gray-900 mb-4">Our Vision</h3>
              <p class="text-gray-600 leading-relaxed">
                To become the most trusted partner in the agricultural export-import industry, known for quality, reliability, and ethical business practices.
              </p>
            </div>
          </div>

          <!-- Products Section -->
          <div class="space-y-8">
            <h2 class="text-3xl md:text-4xl font-semibold text-gray-900 text-center">
              Our Premium Products
            </h2>
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
              <div class="bg-white p-6 rounded-xl shadow-sm">
                <h4 class="text-xl font-semibold text-gray-900 mb-3">Coffee Beans</h4>
                <p class="text-gray-600">
                  Premium Arabica and Robusta coffee beans sourced from the highlands of Cameroon.
                </p>
              </div>
              <div class="bg-white p-6 rounded-xl shadow-sm">
                <h4 class="text-xl font-semibold text-gray-900 mb-3">Cocoa Beans</h4>
                <p class="text-gray-600">
                  Fine-grade cocoa beans perfect for chocolate production and confectionery.
                </p>
              </div>
              <div class="bg-white p-6 rounded-xl shadow-sm">
                <h4 class="text-xl font-semibold text-gray-900 mb-3">Cocoa Products</h4>
                <p class="text-gray-600">
                  Cocoa butter, cocoa mass, cocoa powder, and cocoa shells for various industrial applications.
                </p>
              </div>
            </div>
          </div>

          <!-- Values -->
          <div class="bg-primary/5 p-8 rounded-xl">
            <h2 class="text-3xl md:text-4xl font-semibold text-gray-900 mb-8 text-center">
              Our Core Values
            </h2>
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
              <div class="text-center">
                <div class="w-16 h-16 bg-primary rounded-full flex items-center justify-center mx-auto mb-4">
                  <Icon name="i-heroicons-leaf" class="w-8 h-8 text-white" />
                </div>
                <h4 class="font-semibold text-gray-900 mb-2">Sustainability</h4>
                <p class="text-gray-600 text-sm">
                  Promoting eco-friendly farming practices
                </p>
              </div>
              <div class="text-center">
                <div class="w-16 h-16 bg-primary rounded-full flex items-center justify-center mx-auto mb-4">
                  <Icon name="i-heroicons-shield-check" class="w-8 h-8 text-white" />
                </div>
                <h4 class="font-semibold text-gray-900 mb-2">Quality</h4>
                <p class="text-gray-600 text-sm">
                  Ensuring premium standards in all products
                </p>
              </div>
              <div class="text-center">
                <div class="w-16 h-16 bg-primary rounded-full flex items-center justify-center mx-auto mb-4">
                  <Icon name="i-heroicons-handshake" class="w-8 h-8 text-white" />
                </div>
                <h4 class="font-semibold text-gray-900 mb-2">Integrity</h4>
                <p class="text-gray-600 text-sm">
                  Building trust through honest business
                </p>
              </div>
              <div class="text-center">
                <div class="w-16 h-16 bg-primary rounded-full flex items-center justify-center mx-auto mb-4">
                  <Icon name="i-heroicons-globe-americas" class="w-8 h-8 text-white" />
                </div>
                <h4 class="font-semibold text-gray-900 mb-2">Global Reach</h4>
                <p class="text-gray-600 text-sm">
                  Connecting Cameroon to the world
                </p>
              </div>
            </div>
          </div>

          <!-- CTA Section -->
          <div class="text-center bg-white p-12 rounded-xl shadow-sm">
            <h2 class="text-3xl md:text-4xl font-semibold text-gray-900 mb-4">
              Ready to Partner With Us?
            </h2>
            <p class="text-lg text-gray-600 mb-8">
              Join our network of satisfied clients and experience the quality of Cameroon's finest agricultural products.
            </p>
            <NuxtLink 
              to="/contact"
              class="inline-flex items-center px-8 py-4 bg-primary text-white rounded-lg hover:bg-primary/90 transition-colors group"
            >
              Contact Us
              <Icon name="i-heroicons-arrow-right" class="w-5 h-5 ml-2 transition-transform duration-300 group-hover:translate-x-1" />
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
// Page setup
useHead({
  title: 'About Us - Agri-Management',
  meta: [
    { name: 'description', content: 'Learn about Agri-Management, Cameroon\'s leading export-import company for premium coffee, cocoa, and agricultural products.' }
  ]
})
</script>
