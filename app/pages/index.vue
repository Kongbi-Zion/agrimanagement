<template>
  <div>
    <!-- Additional sections can go here -->
    <section class="py-12 md:py-16 bg-gray-50">
      <div class="container mx-auto px-4">
        <div class="text-center md:text-center max-md:text-left">
          <h1 class="text-3xl md:text-5xl font-semibold text-gray-900 mb-6">Rooted In Cameroon, Trusted <br class="md:block hidden"/> Worldwide</h1>
          <p class="text-md md:pt-8 text-gray-600 max-w-4xl mx-auto max-md:mx-0 px-2 leading-relaxed">
            Agri-Management is a Cameroonian export-import company focused on delivering high-quality cocoa, coffee, and cocoa residues to global markets. With a deep commitment to sustainability and local partnerships, we ensure every product meets international standards of quality and reliability.
          </p>
          <div class="pt-8 md:pt-12 flex md:justify-center w-full">
            <PrimaryButton 
              to="/about"
              text="About Us"
            />
          </div>
        </div>
        <!-- Services Section -->
        <div class="bg-gray-50">
          <UPageSection :ui="{ container: 'px-0!'}">
            <div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
              <UPageCard
                v-for="(service, index) in services"
                :key="index"
                variant="subtle"
                spotlight
                :title="service.title"
                :description="service.description"
                :class="{ 'lg:col-span-2': index === 3 }"
                :icon="service.icon" />
            </div>
          </UPageSection>
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

        <!-- Gallery Section -->
        <UPageSection :ui="{ container: 'px-0!'}">
          <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-4">
            <div
              v-for="(image, index) in galleryImages"
              :key="index"
              class="relative group overflow-hidden rounded-lg"
            >
              <img
                :src="image.src"
                :alt="image.alt"
                class="w-full h-48 object-cover transition-transform duration-300 group-hover:scale-105"
                loading="lazy"
              />
              <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-colors duration-300" />
            </div>
          </div>
        </UPageSection>

 
      </div>
    </section>
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

const galleryImages = ref([
  { src: 'https://media.istockphoto.com/id/1406207995/photo/cocoa-with-chocolate-pieces-and-chocolate-powder-on-the-table.jpg?s=612x612&w=0&k=20&c=TsbVdWD0drv5uIxeIRYYEHDo2NGifx_XdcKQ1QMKUfc=', alt: 'Premium cocoa beans' },
  { src: 'https://media.istockphoto.com/id/503259289/photo/cocoa-in-different-presentations-on-wood-table.jpg?s=612x612&w=0&k=20&c=IwqtT1vqo9S_MNI5ISeT9uGthtFnfAJazQ4wcK7E-PI=', alt: 'Cocoa powder processing' },
  { src: 'https://media.istockphoto.com/id/146969350/photo/cocoa.jpg?s=612x612&w=0&k=20&c=cYCG6VSvo_uoYdQGBaHosAOlZmriVQWu3Te_A-LnfVA=', alt: 'Cocoa butter and mass' },
  { src: 'https://media.istockphoto.com/id/2210604462/photo/fresh-cacao-fruit-growing-in-hawaii.jpg?s=612x612&w=0&k=20&c=PXT8jAshxzSyLT087mfjVBi8Zf23eFWIVivEJSbNajQ=', alt: 'Cocoa shells and residues' },
  { src: 'https://scontent-los4-1.xx.fbcdn.net/v/t39.30808-6/493692947_716490840773515_2302853838345255512_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=13d280&_nc_ohc=muBKFog7o4kQ7kNvwGix-CC&_nc_oc=AdqyWoRZCKEVmS61FuTXeqRt0WqLEvQRYqbFBB1d2UJJhTlHGzwUEtzCA0GoT3wbkJPnII69SZpdBk6Td3k-xtPa&_nc_zt=23&_nc_ht=scontent-los4-1.xx&_nc_gid=BoyW4pgFwCOprp8WqhJuMw&_nc_ss=7a30f&oh=00_Afz0s2Zn9shnJtcuhY40aShA-dTGv-fiW87QQsADsthNVA&oe=69C2C2B9', alt: 'Wedding decorations setup' },
  { src: 'https://media.istockphoto.com/id/1392285553/photo/half-cacao-pods-with-cacao-fruit-and-brown-cocoa-powder.jpg?s=612x612&w=0&k=20&c=AZJlSWpwXQe4aRTWcd6q3MDejVmniif3nQ6fzoFozYI=', alt: 'Event decor and rentals' },
  { src: 'https://m.media-amazon.com/images/I/81KmaTjTRxL._AC_SL1000__.jpg', alt: 'Electronics showroom' },
  { src: 'https://thumbs.dreamstime.com/b/many-used-modern-electronic-gadgets-use-white-floor-reuse-recycle-concept-top-view-153892434.jpg', alt: 'Mobile devices and accessories' }
])

const services = ref([
  {
    title: 'Cocoa',
    description: 'We export high quality Cameroonian cocoa, sustainably sourced and delivered with care to global partners.',
    icon: 'i-heroicons-globe-alt'
  },
  {
    title: 'Cocoa Residues',
    description: 'We export-import quality cocoa residues such as butter, mass, powder, and shells from Cameroon\'s finest cocoa beans.',
    icon: 'i-heroicons-cube'
  },
  {
    title: 'Coffee',
    description: 'We export-import high quality Cameroonian coffee, carefully sourced and processed to meet international quality standards.',
    icon: 'i-heroicons-globe-americas'
  },
  {
    title: 'Decorations',
    description: 'We provide wedding planning, elegant decor for weddings and funerals, plus rentals of chairs, canopies, tables, cutlery, flowers, and décor materials.',
    icon: 'i-heroicons-sparkles'
  },
  {
    title: 'Electronics',
    description: 'We also sell quality electronics, including phones, televisions, phone accessories, woofers, irons, and a wide range of general electronic items.',
    icon: 'i-heroicons-device-phone-mobile'
  }
])

useHead({
  title: 'Agri-Management - Home',
  meta: [
    { name: 'description', content: 'Global trade excellence in agricultural and electronic solutions' }
  ]
})
</script>
