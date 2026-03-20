<template>
  <div class="min-h-screen bg-gray-50">

    <div class="container mx-auto px-4 py-16">
      <div class="max-w-4xl mx-auto">
        <div class="space-y-12">
          <!-- Company Overview -->
                  <div class="text-center md:text-center max-md:text-left">
          <h1 class="text-3xl md:text-5xl font-semibold text-gray-900 mb-6">Agri-Management</h1>
          <p class="text-md md:pt-8 text-gray-600 max-w-4xl mx-auto max-md:mx-0 px-2 leading-relaxed">
            We are a trusted supplier of premium cocoa beans, high-quality coffee, including both Arabica and Robusta varieties and a wide range of cocoa residues and by-products. Our offerings include cocoa mass, cocoa shells, cocoa butter, cocoa powder, and carefully processed coffee beans, all sourced from the fertile regions of Cameroon.
          </p>

        <p class="text-md md:pt-8 text-gray-600 max-w-4xl mx-auto max-md:mx-0 px-2 leading-relaxed">

            Based in Cameroon and officially licensed to export coffee and cocoa, Agri-Management works closely with local farmers and cooperatives to ensure ethical practices, sustainable sourcing, and consistent quality from harvest to export. Our commitment to excellence and traceability has made us a reliable partner for international buyers seeking superior cocoa and coffee products from Central Africa.
          </p>
          
        </div>

        <!-- Our Team -->
        <div class="text-center">
          <h2 class="text-3xl md:text-4xl font-semibold text-gray-900 mb-8">Our Team</h2>
          <p class="text-lg text-gray-600 max-w-4xl mx-auto leading-relaxed">
            At Agri-Management, our team is made up of passionate professionals dedicated to excellence in agricultural export-import. From sourcing specialists and quality control experts to logistics coordinators and client service representatives, each member plays a vital role in delivering top-quality cocoa, coffee, and residues to our global partners. Together, we combine local knowledge with international standards to ensure reliability, transparency, and long-term success.
          </p>
        </div>

        <!-- CTA Sections -->
        <UPageSection :ui="{ container: 'p-0!'}">
          <UPageCTA
            v-for="(cta, index) in ctaSections"
            :key="index"
            :title="cta.title"
            :description="cta.description"
            orientation="horizontal"
            :links="cta.to ? [{ label: 'Learn more', color: 'secondary', variant: 'subtle', trailingIcon: 'i-lucide-arrow-right', to: cta.to }] : links"
            class="ring-0! bg-transparent"
            :reverse="cta.reverse"
            :ui="{ container: 'px-0!' }"
          >
            <img
              :src="cta.image"
              width="320"
              height="364"
              :alt="cta.alt"
              class="w-full rounded-lg h-70 md:h-150 object-cover"
              loading="lazy"
            />
          </UPageCTA>
        </UPageSection>

        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { ButtonProps } from '@nuxt/ui'

const links = ref<ButtonProps[]>([
  {
    label: 'Learn more',
    color: 'neutral',
    variant: 'subtle',
    trailingIcon: 'i-lucide-arrow-right'
  }
])

const ctaSections = ref([
  {
    title: 'Coffee, Cocoa & Residues',
    description: 'We export-import Cameroonian coffee, cocoa beans, cocoa mass, cocoa butter, cocoa powder, and cocoa shells.',
    image: '/hero-bg.jpg',
    alt: 'Illustration',
    reverse: false,
    to: '/cocoa-coffee'
  },
  {
    title: 'Event Decor & Rentals',
    description: 'We offer event decor and rentals, specializing in creating unforgettable moments for weddings, birthdays, and special events of all kinds. With a keen eye for detail and a passion for transforming spaces, we offer a wide range of decorative elements, from elegant floral arrangements and stylish furniture to lighting, arches, and themed props. Whether you\'re planning an intimate celebration or a large-scale event, our dedicated team works closely with clients to bring every vision to life with creativity, professionalism, and care. From planning and design to delivery and setup, our goal is to make your special day seamless and stunning. Let us help you turn your next event into a beautiful memory.',
    image: '/decor.jpg',
    alt: 'Event Decor & Rentals',
    reverse: true,
    to: '/decors'
  },
  {
    title: 'Premium Electronics',
    description: 'Discover our curated selection of high-quality electronics, from the latest smartphones and laptops to home appliances and accessories. We combine cutting-edge technology with competitive pricing to deliver premium products that enhance your digital lifestyle and productivity.',
    image: '/electronic.jpg',
    alt: 'Premium Electronics',
    reverse: false,
    to: '/electronics'
  }
])

// Page setup
useHead({
  title: 'About Us - Agri-Management',
  meta: [
    { name: 'description', content: 'Learn about Agri-Management, Cameroon\'s leading export-import company for premium coffee, cocoa, and agricultural products.' }
  ]
})
</script>
