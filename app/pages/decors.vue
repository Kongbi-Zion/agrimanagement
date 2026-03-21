<template>
  <div class="max-w-6xl mx-auto space-y-8 py-8">
    <div class="text-start md:text-center mb-12">
      <h1 class="text-3xl md:text-4xl font-semibold text-gray-900 mb-4">Beautiful Celebrations, Thoughtfully Designed</h1>
      <p class="text-xl text-gray-600 max-w-4xl mx-auto pt-5">
        We provide full-service event décor and planning, tailored to make every moment unforgettable. Whether it's a grand wedding, a heartfelt funeral, or a joyful celebration, we transform your vision into reality with elegance and care.
      </p>
    </div>

    <section class="bg-gray-50 p-8 rounded-lg mb-12">
      <h2 class="text-2xl font-semibold mb-8 text-center">Our Specialties</h2>
      <div class="grid pt-8 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div
          v-for="specialty in specialties"
          :key="specialty.title"
          class="text-center"
        >
          <div :class="`w-16 h-16 ${specialty.bgColor} rounded-full flex items-center justify-center mx-auto mb-4`">
            <Icon :name="specialty.icon" :class="`w-8 h-8 ${specialty.iconColor}`" />
          </div>
          <h3 class="text-lg font-semibold mb-2">{{ specialty.title }}</h3>
          <p class="text-gray-600 text-sm">
            {{ specialty.description }}
          </p>
        </div>
      </div>
    </section>

    <section class="bg-white p-8 rounded-lg shadow-sm border border-gray-200 mb-12">
      <h2 class="text-2xl font-semibold mb-6 text-center">Rental Services</h2>
      <p class="text-gray-600 mb-8 text-center max-w-3xl mx-auto">
        To support your event needs, we also offer a comprehensive range of rental services, including chairs, canopies, tables, cutlery, chafing dishes, flowers, and all essential décor materials.
      </p>
      <div class="grid md:grid-cols-3 lg:grid-cols-6 gap-4">
        <div
          v-for="rental in rentals"
          :key="rental.name"
          class="text-center p-4 bg-gray-50 rounded-lg"
        >
          <Icon :name="rental.icon" :class="`w-8 h-8 ${rental.iconColor} mx-auto mb-2`" />
          <h4 class="font-medium text-sm">{{ rental.name }}</h4>
        </div>
      </div>
    </section>

    <section>
      <div class="space-y-12">
        <UPageSection
          v-for="(section, index) in sections"
          :key="index"
          :title="section.title"
          :description="section.description"
          :icon="section.icon"
          orientation="horizontal"
          :reverse="index % 2 === 1"
          :features="section.features"
          :links="section.links"
        >
          <video
            :src="section.video"
            width="352"
            height="647"
            :alt="section.alt"
            class="w-full rounded-lg h-70 md:h-150 object-cover"
            controls
            autoplay
            muted
            loop
            loading="lazy"
          />
        </UPageSection>
      </div>
    </section>

        <section class="text-center py-12">
      <h2 class="text-2xl font-semibold mb-6">Stress-Free Celebrations</h2>
      <p class="text-gray-600 mb-8 max-w-3xl mx-auto">
        From intimate gatherings to large-scale ceremonies, we deliver thoughtful designs and dependable service—so you can enjoy your special day without stress.
      </p>
      <div class="flex justify-center space-x-4">
        <UButton to="/contact" size="lg" color="primary">
          Plan Your Event
        </UButton>
        <UButton to="tel:683021474" size="lg" variant="outline">
          Call Us Now
        </UButton>
      </div>
    </section>
  </div>
</template>

<script setup>
const sections = ref([
  {
    title: 'Birthday Decor\'s',
    description: 'Celebrate in style with vibrant, personalized decorations perfect for any age or theme, from kids\' parties to elegant adult birthdays.',
    icon: 'i-heroicons-gift',
    video: '/videos/birthday.mp4',
    alt: 'Birthday Decorations',
    features: [
      {
        title: 'Themed Decorations',
        description: 'Custom themes for all ages and preferences',
        icon: 'i-heroicons-sparkles',
        to: '#'
      },
      {
        title: 'Personalized Setup',
        description: 'Tailored decorations to match your vision',
        icon: 'i-heroicons-paint-brush',
        to: '#'
      },
      {
        title: 'Complete Packages',
        description: 'All-inclusive decoration services',
        icon: 'i-heroicons-cube',
        to: '#'
      }
    ],
    links: [
      {
        label: 'Contact us on WhatsApp',
        to: 'https://wa.me/683021474',
        color: 'primary',
        variant: 'solid',
        trailingIcon: 'i-lucide-message-circle'
      }
    ]
  },
  {
    title: 'Wedding Receptions Decor\'s',
    description: 'Elegant and timeless setups designed to transform your reception into a stunning and unforgettable experience for you and your guests.',
    icon: 'i-heroicons-heart',
    video: '/videos/reception.mp4',
    alt: 'Wedding Reception Decorations',
    features: [
      {
        title: 'Elegant Centerpieces',
        description: 'Stunning floral arrangements and table decor',
        icon: 'i-heroicons-flower',
        to: '#'
      },
      {
        title: 'Lighting Design',
        description: 'Ambient lighting for perfect mood',
        icon: 'i-heroicons-light-bulb',
        to: '#'
      },
      {
        title: 'Table Settings',
        description: 'Beautiful place settings and arrangements',
        icon: 'i-heroicons-rectangle-stack',
        to: '#'
      }
    ],
    links: [
      {
        label: 'Contact Us',
        to: 'https://wa.me/683021474',
        color: 'primary',
        variant: 'solid',
        trailingIcon: 'i-lucide-message-circle'
      }
    ]
  },
  {
    title: 'Traditional Wedding Decor\'s',
    description: 'Culturally inspired decorations that honor your roots, rich in color, symbolism, and tradition, tailored to your heritage and celebration style.',
    icon: 'i-heroicons-sparkles',
    video: '/videos/traditional.mp4',
    alt: 'Traditional Wedding Decorations',
    features: [
      {
        title: 'Cultural Elements',
        description: 'Authentic traditional decorations',
        icon: 'i-heroicons-globe-americas',
        to: '#'
      },
      {
        title: 'Symbolic Colors',
        description: 'Rich colors with cultural significance',
        icon: 'i-heroicons-palette',
        to: '#'
      },
      {
        title: 'Heritage Style',
        description: 'Time-honored decoration traditions',
        icon: 'i-heroicons-star',
        to: '#'
      }
    ],
    links: [
      {
        label: 'Contact Us',
        to: 'https://wa.me/683021474',
        color: 'primary',
        variant: 'solid',
        trailingIcon: 'i-lucide-message-circle'
      }
    ]
  },
  {
    title: 'Church Wedding Decor\'s',
    description: 'Graceful and minimal designs that enhance your sacred ceremony space with beauty, elegance, and spiritual reverence.',
    icon: 'i-heroicons-building-office',
    video: '/videos/church.mp4',
    alt: 'Church Wedding Decorations',
    features: [
      {
        title: 'Sacred Elements',
        description: 'Reverent church-appropriate decorations',
        icon: 'i-heroicons-candle',
        to: '#'
      },
      {
        title: 'Elegant Arrangements',
        description: 'Graceful floral and fabric designs',
        icon: 'i-heroicons-flower',
        to: '#'
      },
      {
        title: 'Spiritual Atmosphere',
        description: 'Peaceful and respectful environment',
        icon: 'i-heroicons-heart',
        to: '#'
      }
    ],
    links: [
      {
        label: 'Contact Us',
        to: 'https://wa.me/683021474',
        color: 'primary',
        variant: 'solid',
        trailingIcon: 'i-lucide-message-circle'
      }
    ]
  }
])

const rentals = ref([
  {
    name: 'Chairs',
    icon: 'i-heroicons-cube',
    iconColor: 'text-indigo-600'
  },
  {
    name: 'Canopies',
    icon: 'i-heroicons-home',
    iconColor: 'text-blue-600'
  },
  {
    name: 'Tables',
    icon: 'i-heroicons-table-cells',
    iconColor: 'text-green-600'
  },
  {
    name: 'Cutlery',
    icon: 'i-heroicons-squares-2x2',
    iconColor: 'text-amber-600'
  },
  {
    name: 'Chafing Dishes',
    icon: 'i-heroicons-fire',
    iconColor: 'text-orange-600'
  },
  {
    name: 'Flowers',
    icon: 'i-heroicons-gift',
    iconColor: 'text-pink-600'
  }
])

const specialties = ref([
  {
    title: 'Wedding Planning',
    description: 'Seamless coordination from start to finish',
    icon: 'i-heroicons-heart',
    bgColor: 'bg-pink-100',
    iconColor: 'text-pink-600'
  },
  {
    title: 'Traditional Wedding Décor',
    description: 'Celebrates cultural beauty and heritage',
    icon: 'i-heroicons-sparkles',
    bgColor: 'bg-purple-100',
    iconColor: 'text-purple-600'
  },
  {
    title: 'Church Wedding Décor',
    description: 'Designed with grace and reverence',
    icon: 'i-heroicons-building-office',
    bgColor: 'bg-blue-100',
    iconColor: 'text-blue-600'
  },
  {
    title: 'Funeral Décor',
    description: 'Comfort and dignity for final tributes',
    icon: 'i-heroicons-sparkles',
    bgColor: 'bg-gray-100',
    iconColor: 'text-gray-600'
  }
])

useHead({
  title: 'Decor\'s - Agri-Management',
  meta: [
    { name: 'description', content: 'Beautiful decorative items and home accessories for elegant living spaces' }
  ]
})
</script>
