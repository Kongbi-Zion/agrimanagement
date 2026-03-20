<template>
  <div class="max-w-6xl mx-auto space-y-8 py-12">
    <div class="text-center mb-16">
      <h1 class="text-3xl md:text-5xl font-semibold text-gray-900 mb-6">Get In Touch</h1>
      <p class="text-md text-gray-600 max-w-2xl mx-auto px-2 leading-relaxed">
        Contact us through any of the following channels, and our team will get back to you promptly.
      </p>
    </div>

    <div class="grid md:grid-cols-3 gap-8 mb-12">
      <div 
        v-for="contact in contactInfo" 
        :key="contact.title"
        class="bg-white px-10 py-8 rounded-xl border border-gray-100 text-center"
      >
        <div class="inline-flex items-center justify-center w-12 h-12 bg-secondary/10 rounded-full mb-4">
          <Icon :name="contact.icon" class="w-6 h-6 text-primary" />
        </div>
        <h3 class="font-semibold text-gray-900 mb-2">{{ contact.title }}</h3>
        <div v-if="Array.isArray(contact.content)" class="text-gray-600 space-y-1">
          <p v-for="item in contact.content" :key="item">{{ item }}</p>
        </div>
        <p v-else class="text-gray-600">{{ contact.content }}</p>
      </div>
    </div>

    <div class="bg-white rounded-xl border border-gray-100 p-8">
      <h2 class="text-2xl font-semibold text-gray-900 mb-8 text-center">Get in Touch Directly</h2>
      <div class="grid md:grid-cols-2 gap-6">
        <a
          href="https://wa.me/237681553888"
          target="_blank"
          rel="noopener noreferrer"
          class="flex items-center justify-center px-6 py-4 bg-green-500 text-white rounded-lg hover:bg-green-600 transition-colors group"
        >
          <Icon name="i-simple-icons-whatsapp" class="w-6 h-6 mr-3" />
          <span class="font-medium">Chat on WhatsApp</span>
          <Icon name="i-heroicons-arrow-right" class="w-5 h-5 ml-2 transition-transform duration-300 group-hover:translate-x-1" />
        </a>
        
        <a
          href="mailto:divinyuy@yahoo.com"
          class="flex items-center justify-center px-6 py-4 bg-primary text-white rounded-lg hover:bg-primary/90 transition-colors group"
        >
          <Icon name="i-heroicons-envelope" class="w-6 h-6 mr-3" />
          <span class="font-medium">Send Email</span>
          <Icon name="i-heroicons-arrow-right" class="w-5 h-5 ml-2 transition-transform duration-300 group-hover:translate-x-1" />
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>
const contactInfo = [
  {
    title: 'Our Location',
    icon: 'i-heroicons-map-pin',
    content: 'Douala - Bonaberi'
  },
  {
    title: 'Call Us On',
    icon: 'i-heroicons-phone',
    content: ['+237 681 55 38 88', '+237 671 35 15 81']
  },
  {
    title: 'Email Us',
    icon: 'i-heroicons-envelope',
    content: 'divinyuy@yahoo.com'
  }
]

useHead({
  title: 'Contact - Agri-Management',
  meta: [
    { name: 'description', content: 'Get in touch with our team for inquiries and partnerships' }
  ]
})
</script>
