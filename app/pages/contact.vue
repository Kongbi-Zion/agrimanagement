<template>
  <div class="max-w-4xl mx-auto space-y-8 py-8">
    <div class="text-center mb-12">
      <h1 class="text-4xl font-bold text-gray-900 mb-4">Contact Us</h1>
      <p class="text-xl text-gray-600">
        Get in touch with our team for inquiries and partnerships
      </p>
    </div>

    <div class="grid md:grid-cols-2 gap-8">
      <section>
        <h2 class="text-2xl font-semibold mb-6">Send us a Message</h2>
        <form class="space-y-6" @submit.prevent="handleSubmit">
          <div>
            <label for="name" class="block text-sm font-medium text-gray-700 mb-2">Full Name</label>
            <input
              id="name"
              v-model="form.name"
              type="text"
              required
              class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent"
              placeholder="John Doe"
            />
          </div>

          <div>
            <label for="email" class="block text-sm font-medium text-gray-700 mb-2">Email Address</label>
            <input
              id="email"
              v-model="form.email"
              type="email"
              required
              class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent"
              placeholder="john@example.com"
            />
          </div>

          <div>
            <label for="subject" class="block text-sm font-medium text-gray-700 mb-2">Subject</label>
            <select
              id="subject"
              v-model="form.subject"
              required
              class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent"
            >
              <option value="">Select a topic</option>
              <option value="cocoa-coffee">Cocoa & Coffee Inquiry</option>
              <option value="electronics">Electronics Inquiry</option>
              <option value="decors">Decor's Inquiry</option>
              <option value="partnership">Partnership Opportunity</option>
              <option value="general">General Inquiry</option>
            </select>
          </div>

          <div>
            <label for="message" class="block text-sm font-medium text-gray-700 mb-2">Message</label>
            <textarea
              id="message"
              v-model="form.message"
              rows="5"
              required
              class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent"
              placeholder="Tell us about your inquiry..."
            ></textarea>
          </div>

          <UButton type="submit" size="lg" color="primary" :loading="isSubmitting" :disabled="isSubmitting">
            {{ isSubmitting ? 'Sending...' : 'Send Message' }}
          </UButton>
        </form>
      </section>

      <section>
        <h2 class="text-2xl font-semibold mb-6">Contact Information</h2>
        <div class="space-y-6">
          <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
            <div class="flex items-center space-x-3 mb-3">
              <div class="w-10 h-10 bg-blue-100 rounded-full flex items-center justify-center">
                <Icon name="i-heroicons-envelope" class="w-5 h-5 text-blue-600" />
              </div>
              <h3 class="font-semibold">Email</h3>
            </div>
            <p class="text-gray-600">info@agri-management.com</p>
            <p class="text-gray-600">sales@agri-management.com</p>
          </div>

          <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
            <div class="flex items-center space-x-3 mb-3">
              <div class="w-10 h-10 bg-green-100 rounded-full flex items-center justify-center">
                <Icon name="i-heroicons-phone" class="w-5 h-5 text-green-600" />
              </div>
              <h3 class="font-semibold">Phone</h3>
            </div>
            <p class="text-gray-600">+1 (555) 123-4567</p>
            <p class="text-gray-600">+44 20 7123 4567 (UK)</p>
          </div>

          <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
            <div class="flex items-center space-x-3 mb-3">
              <div class="w-10 h-10 bg-purple-100 rounded-full flex items-center justify-center">
                <Icon name="i-heroicons-map-pin" class="w-5 h-5 text-purple-600" />
              </div>
              <h3 class="font-semibold">Office Locations</h3>
            </div>
            <div class="space-y-3">
              <div>
                <p class="font-semibold text-gray-900">Headquarters</p>
                <p class="text-gray-600">123 Business Avenue, Commerce City, CC 12345</p>
              </div>
              <div>
                <p class="font-semibold text-gray-900">European Office</p>
                <p class="text-gray-600">456 Trade Street, London, UK EC1A 1BB</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>

    <section class="bg-gray-50 p-8 rounded-lg">
      <h2 class="text-2xl font-semibold mb-6 text-center">Business Hours</h2>
      <div class="grid md:grid-cols-2 gap-8">
        <div>
          <h3 class="font-semibold mb-3">Customer Support</h3>
          <div class="space-y-2">
            <div class="flex justify-between">
              <span class="text-gray-600">Monday - Friday</span>
              <span class="font-medium">9:00 AM - 6:00 PM</span>
            </div>
            <div class="flex justify-between">
              <span class="text-gray-600">Saturday</span>
              <span class="font-medium">10:00 AM - 4:00 PM</span>
            </div>
            <div class="flex justify-between">
              <span class="text-gray-600">Sunday</span>
              <span class="font-medium">Closed</span>
            </div>
          </div>
        </div>
        <div>
          <h3 class="font-semibold mb-3">Sales & Partnerships</h3>
          <div class="space-y-2">
            <div class="flex justify-between">
              <span class="text-gray-600">Monday - Friday</span>
              <span class="font-medium">8:00 AM - 8:00 PM</span>
            </div>
            <div class="flex justify-between">
              <span class="text-gray-600">Saturday</span>
              <span class="font-medium">9:00 AM - 5:00 PM</span>
            </div>
            <div class="flex justify-between">
              <span class="text-gray-600">Sunday</span>
              <span class="font-medium">10:00 AM - 2:00 PM</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="text-center py-12">
      <h2 class="text-2xl font-semibold mb-6">Connect With Us</h2>
      <p class="text-gray-600 mb-8">
        Follow us on social media for updates and industry insights
      </p>
      <div class="flex justify-center space-x-4">
        <a href="#" class="text-white bg-blue-600 hover:bg-blue-700 p-3 rounded-full transition-colors">
          <Icon name="i-simple-icons-facebook" class="w-5 h-5" />
        </a>
        <a href="#" class="text-white bg-black hover:bg-gray-800 p-3 rounded-full transition-colors">
          <Icon name="i-simple-icons-x" class="w-5 h-5" />
        </a>
        <a href="#" class="text-white bg-blue-700 hover:bg-blue-800 p-3 rounded-full transition-colors">
          <Icon name="i-simple-icons-linkedin" class="w-5 h-5" />
        </a>
      </div>
    </section>
  </div>
</template>

<script setup>
const form = ref({
  name: '',
  email: '',
  subject: '',
  message: ''
})

const isSubmitting = ref(false)

const handleSubmit = async () => {
  isSubmitting.value = true
  
  // Simulate form submission
  await new Promise(resolve => setTimeout(resolve, 2000))
  
  // Here you would typically send the form data to your backend
  console.log('Form submitted:', form.value)
  
  // Reset form
  form.value = {
    name: '',
    email: '',
    subject: '',
    message: ''
  }
  
  isSubmitting.value = false
  
  // You could show a success message here
  alert('Thank you for your message! We will get back to you soon.')
}

useHead({
  title: 'Contact - Agri-Management',
  meta: [
    { name: 'description', content: 'Get in touch with our team for inquiries and partnerships' }
  ]
})
</script>
