<template>
  <div class="max-w-6xl mx-auto space-y-8 py-8">
    <div class="text-center mb-12">
      <h1 class="text-4xl font-bold text-gray-900 mb-4">Premium Electronics</h1>
      <p class="text-xl text-gray-600">
        Discover our curated selection of high-quality electronics, from smartphones to home appliances
      </p>
    </div>

    <section class="bg-gray-50 p-8 rounded-lg">
      <h2 class="text-2xl font-semibold mb-6 text-center">Why Choose Our Electronics?</h2>
      <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div class="text-center">
          <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
            <Icon name="i-heroicons-check-circle" class="w-6 h-6 text-blue-600" />
          </div>
          <h4 class="font-semibold mb-2">Quality Guaranteed</h4>
          <p class="text-gray-600 text-sm">
            All products are genuine and come with warranty
          </p>
        </div>
        <div class="text-center">
          <div class="w-12 h-12 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
            <Icon name="i-heroicons-truck" class="w-6 h-6 text-green-600" />
          </div>
          <h4 class="font-semibold mb-2">Fast Delivery</h4>
          <p class="text-gray-600 text-sm">
            Quick and reliable delivery across Cameroon
          </p>
        </div>
        <div class="text-center">
          <div class="w-12 h-12 bg-purple-100 rounded-full flex items-center justify-center mx-auto mb-4">
            <Icon name="i-heroicons-currency-dollar" class="w-6 h-6 text-purple-600" />
          </div>
          <h4 class="font-semibold mb-2">Competitive Prices</h4>
          <p class="text-gray-600 text-sm">
            Best prices for quality electronics
          </p>
        </div>
        <div class="text-center">
          <div class="w-12 h-12 bg-yellow-100 rounded-full flex items-center justify-center mx-auto mb-4">
            <Icon name="i-heroicons-headset" class="w-6 h-6 text-yellow-600" />
          </div>
          <h4 class="font-semibold mb-2">Customer Support</h4>
          <p class="text-gray-600 text-sm">
            Dedicated support for all your needs
          </p>
        </div>
      </div>
    </section>

    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
      <div
        v-for="(product, index) in products"
        :key="index"
        class="bg-white rounded-lg shadow-sm border border-gray-200 overflow-hidden hover:shadow-lg transition-shadow"
      >
        <div :class="`h-48 bg-linear-to-br ${product.gradient} flex items-center justify-center relative overflow-hidden`">
          <img 
            v-if="product.image" 
            :src="product.image" 
            :alt="product.title"
            class="absolute inset-0 w-full h-full object-cover opacity-80"
          />
          <Icon 
            v-else
            :name="product.icon" 
            :class="`w-16 h-16 ${product.iconColor} relative z-10`" 
          />
        </div>
        <div class="p-6">
          <h3 class="text-lg font-semibold mb-2">{{ product.title }}</h3>
          <p class="text-gray-600 mb-4">{{ product.description }}</p>
          <ul class="space-y-1 text-sm text-gray-500 mb-4">
            <li v-for="feature in product.features" :key="feature">• {{ feature }}</li>
          </ul>
          <UButton to="/contact" size="sm" variant="outline">Inquire Now</UButton>
        </div>
      </div>
    </div>

    <section class="text-center py-12">
      <h2 class="text-2xl font-semibold mb-6">Looking for Something Specific?</h2>
      <p class="text-gray-600 mb-8 max-w-3xl mx-auto">
        Can't find what you're looking for? Contact us with your requirements and we'll source it for you from our extensive network of suppliers.
      </p>
      <div class="flex flex-col sm:flex-row gap-4 justify-center items-center text-center">
        <UButton to="/contact" size="lg" color="primary">Get a Quote</UButton>
        <UButton to="tel:+237681553888" size="lg" variant="outline">Call Us Now</UButton>
      </div>
    </section>
  </div>
</template>

<script setup>
const products = ref([
  {
    title: 'Smartphones & Tablets',
    description: 'Latest smartphones and tablets from top brands with cutting-edge features.',
    icon: 'i-heroicons-device-phone-mobile',
    iconColor: 'text-blue-600',
    image: 'https://www.tbsnews.net/sites/default/files/styles/big_2/public/images/2025/11/20/phone.png',
    gradient: 'from-blue-100 to-blue-200',
    features: ['5G connectivity', 'High-resolution cameras', 'Premium displays']
  },
  {
    title: 'Laptops & Computers',
    description: 'High-performance laptops and desktop computers for work and gaming.',
    icon: 'i-heroicons-computer-desktop',
    iconColor: 'text-green-600',
    image: 'https://static.wixstatic.com/media/33caa3_9ab19a2c88b847b59d7fdfb62b067d41~mv2.jpg/v1/fill/w_640,h_456,al_c,q_80,usm_0.66_1.00_0.01,enc_avif,quality_auto/33caa3_9ab19a2c88b847b59d7fdfb62b067d41~mv2.jpg',
    gradient: 'from-green-100 to-green-200',
    features: ['Intel & AMD processors', 'SSD storage', 'Dedicated graphics']
  },
  {
    title: 'Televisions & Displays',
    description: 'Smart TVs and monitors with stunning 4K/8K resolution.',
    icon: 'i-heroicons-tv',
    iconColor: 'text-purple-600',
    image: '/electronic.jpg',
    gradient: 'from-purple-100 to-purple-200',
    features: ['Smart TV features', 'HDR technology', 'Multiple screen sizes']
  },
  {
    title: 'Audio Equipment',
    description: 'Premium speakers, woofers, and audio accessories.',
    icon: 'i-heroicons-speaker-wave-2',
    iconColor: 'text-yellow-600',
    image: 'https://hips.hearstapps.com/hmg-prod/images/wireless-earbuds-001-6792869accae0.jpg?crop=0.583xw:0.776xh;0.194xw,0.179xh&resize=1200:*',
    gradient: 'from-yellow-100 to-yellow-200',
    features: ['Bluetooth connectivity', 'Surround sound', 'Professional quality']
  },
  {
    title: 'Home Appliances',
    description: 'Essential home appliances including irons, kettles, and more.',
    icon: 'i-heroicons-home',
    iconColor: 'text-red-600',
    image: 'https://konnra.com/wp-content/uploads/2024/09/Modern-Kitchen-Appliances.png',
    gradient: 'from-red-100 to-red-200',
    features: ['Energy efficient', 'Modern designs', 'Reliable brands']
  },
  {
    title: 'Accessories & More',
    description: 'Phone accessories, cables, chargers, and electronic components.',
    icon: 'i-heroicons-cog-6-tooth',
    iconColor: 'text-indigo-600',
    image: 'https://miro.medium.com/v2/resize:fit:1200/1*TtiUAqywBXI2OX1nSOz1lg.jpeg',
    gradient: 'from-indigo-100 to-indigo-200',
    features: ['Phone accessories', 'Computer peripherals', 'Electronic components']
  }
])

useHead({
  title: 'Electronics - Agri-Management',
  meta: [
    { name: 'description', content: 'Cutting-edge electronic components and solutions for modern industries' }
  ]
})
</script>
