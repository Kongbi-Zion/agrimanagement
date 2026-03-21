<template>
  <div class="max-w-6xl mx-auto space-y-8 py-8">
    <div class="text-center md:text-center max-md:text-left">
      <h1 class="text-3xl md:text-5xl font-semibold text-gray-900 mb-6">Trade Has Never Tasted So Good</h1>
      <p class="text-md md:pt-5 text-gray-600 max-w-4xl mx-auto max-md:mx-0 px-2 leading-relaxed">
        We export-import Cameroon's finest coffee and cocoa products, sustainably sourced, expertly propposed, and globally trusted.
      </p>
    </div>

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
        <img
          :src="section.image"
          width="352"
          height="647"
          :alt="section.alt"
          class="w-full rounded-lg h-70 md:h-150 object-cover"
          loading="lazy"
        />
      </UPageSection>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { PageFeatureProps, ButtonProps } from '@nuxt/ui'

const sections = ref([
  {
    title: 'Coffee Beans',
    description: 'High-quality Cameroonian coffee, available in both Arabica and Robusta varieties, known for its rich flavor and smooth aroma.',
    icon: 'i-lucide-coffee',
    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS8O3kwanWqBmMEpqxtXA3qL9n5RgXTehYqjA&s',
    alt: 'Coffee Beans',
    features: [
      {
        title: 'High Altitude Sourcing',
        description: 'Sourced from high-altitude farms in Cameroon',
        icon: 'i-lucide-mountain',
        to: '#'
      },
      {
        title: 'Careful Processing',
        description: 'Carefully harvested and processed',
        icon: 'i-lucide-settings',
        to: '#'
      },
      {
        title: 'Versatile Forms',
        description: 'Available in green or roasted form',
        icon: 'i-lucide-package',
        to: '#'
      },
      {
        title: 'Multi-Purpose',
        description: 'Suitable for specialty or commercial use',
        icon: 'i-lucide-briefcase',
        to: '#'
      }
    ],
    links: [
      {
        label: 'Contact us on WhatsApp',
        to: 'https://wa.me/237681553888',
        color: 'primary' as const,
        variant: 'solid' as const,
        trailingIcon: 'i-lucide-message-circle'
      }
    ]
  },
  {
    title: 'Cocoa Powder',
    description: 'De-fatted cocoa used in beverages, baking, and confectionery, offering a strong chocolate aroma and taste.',
    icon: 'i-lucide-powder',
    image: 'https://www.dellomano.com.au/cdn/shop/articles/ultimate-guide-to-choosing-the-perfect-cocoa-powder-for-baking-8964736.png?v=1773368593',
    alt: 'Cocoa Powder',
    features: [
      {
        title: 'Low-Fat Content',
        description: 'Low-fat, unsweetened powder',
        icon: 'i-lucide-heart',
        to: '#'
      },
      {
        title: 'Natural Flavor',
        description: 'Processed to retain natural flavor',
        icon: 'i-lucide-leaf',
        to: '#'
      },
      {
        title: 'Food & Beverage',
        description: 'Suitable for food and beverage industries',
        icon: 'i-lucide-utensils',
        to: '#'
      },
      {
        title: 'Bulk Packaging',
        description: 'Packaged in various bulk sizes',
        icon: 'i-lucide-boxes',
        to: '#'
      }
    ],
    links: [
      {
        label: 'Contact us on WhatsApp',
        to: 'https://wa.me/237681553888',
        color: 'primary' as const,
        variant: 'solid' as const,
        trailingIcon: 'i-lucide-message-circle'
      }
    ]
  },
  {
    title: 'Cocoa Mass',
    description: 'Finely ground, pure cocoa used in the production of chocolate and other cocoa-based products.',
    icon: 'i-lucide-circle',
    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSlAATt4wiK0pj-tEv9buKmfkF0IBq1WfbdOg&s',
    alt: 'Cocoa Mass',
    features: [
      {
        title: '100% Pure',
        description: '100% pure cocoa content',
        icon: 'i-lucide-check-circle',
        to: '#'
      },
      {
        title: 'Intense Flavor',
        description: 'Deep, intense chocolate flavor',
        icon: 'i-lucide-flame',
        to: '#'
      },
      {
        title: 'Versatile Use',
        description: 'Ideal for industrial or artisanal use',
        icon: 'i-lucide-globe',
        to: '#'
      },
      {
        title: 'No Additives',
        description: 'No additives or preservatives',
        icon: 'i-lucide-shield-check',
        to: '#'
      }
    ],
    links: [
      {
        label: 'Contact us on WhatsApp',
        to: 'https://wa.me/237681553888',
        color: 'primary' as const,
        variant: 'solid' as const,
        trailingIcon: 'i-lucide-message-circle'
      }
    ]
  },
  {
    title: 'Cocoa Shells',
    description: 'A natural by-product of cocoa bean processing, used for mulch, animal feed, or tea infusions.',
    icon: 'i-lucide-circle-off',
    image: 'https://auburnoaksgardencenter.com/cdn/shop/files/PXL_20230505_125209752.PORTRAIT.jpg?v=1683292707',
    alt: 'Cocoa Shells',
    features: [
      {
        title: 'Eco-Friendly',
        description: 'Eco-friendly and biodegradable',
        icon: 'i-lucide-leaf',
        to: '#'
      },
      {
        title: 'High Speed Internet',
        description: 'Rich in antioxidants and fiber',
        icon: 'i-lucide-wifi',
        to: '#'
      },
      {
        title: 'Bulk Available',
        description: 'Available in bulk quantities',
        icon: 'i-lucide-package-2',
        to: '#'
      }
    ],
    links: [
      {
        label: 'Contact us on WhatsApp',
        to: 'https://wa.me/237681553888',
        color: 'primary' as const,
        variant: 'solid' as const,
        trailingIcon: 'i-lucide-message-circle'
      }
    ]
  },
  {
    title: 'Cocoa Butter',
    description: 'A smooth, aromatic fat extracted from cocoa beans, widely used in chocolate production, cosmetics, and pharmaceuticals.',
    icon: 'i-lucide-droplet',
    image: 'https://cdn.britannica.com/74/192174-050-E0FBB833/cocoa-butter-beans.jpg',
    alt: 'Cocoa Butter',
    features: [
      {
        title: 'Food Grade Quality',
        description: '100% pure and food-grade quality',
        icon: 'i-lucide-award',
        to: '#'
      },
      {
        title: 'Creamy Texture',
        description: 'Creamy texture with mild chocolate scent',
        icon: 'i-lucide-sparkles',
        to: '#'
      },
      {
        title: 'Multiple Uses',
        description: 'Ideal for chocolate, skincare, and soaps',
        icon: 'i-lucide-infinity',
        to: '#'
      },
      {
        title: 'Various Forms',
        description: 'Available in blocks, chips, or bulk packaging',
        icon: 'i-lucide-boxes',
        to: '#'
      }
    ],
    links: [
      {
        label: 'Contact Us',
        to: '/contact',
        color: 'primary' as const,
        variant: 'solid' as const,
        trailingIcon: 'i-lucide-arrow-right'
      }
    ]
  }
])

const features = ref<PageFeatureProps[]>([
  {
    title: 'Icons',
    description: 'Nuxt UI integrates with Nuxt Icon to access over 200,000+ icons from Iconify.',
    icon: 'i-lucide-smile',
    to: '/docs/getting-started/integrations/icons'
  },
  {
    title: 'Fonts',
    description: 'Nuxt UI integrates with Nuxt Fonts to provide plug-and-play font optimization.',
    icon: 'i-lucide-a-large-small',
    to: '/docs/getting-started/integrations/fonts'
  },
  {
    title: 'Color Mode',
    description: 'Nuxt UI integrates with Nuxt Color Mode to switch between light and dark.',
    icon: 'i-lucide-sun-moon',
    to: '/docs/getting-started/integrations/color-mode'
  }
])

const links = ref<ButtonProps[]>([
  {
    label: 'Explore components',
    to: '/docs/components/app',
    color: 'neutral',
    variant: 'subtle',
    trailingIcon: 'i-lucide-arrow-right'
  }
])

useHead({
  title: 'Cocoa & Coffee - Agri-Management',
  meta: [
    { name: 'description', content: 'Premium quality cocoa and coffee products for global markets' }
  ]
})
</script>
