<template>
  <div class="min-h-screen bg-gray-50">
    <HeroSection v-if="$route.path === '/'" />
    <HeaderSection 
      v-else 
      :title="getPageTitle()" 
      :description="getPageDescription()" 
      :backgroundImage="getBackgroundImage()"
    />
    
    <main class="container mx-auto px-4 py-8">
      <slot />
    </main>
    <AppFooter />
    <WhatsAppButton />
  </div>
</template>

<script setup lang="ts">
const route = useRoute()

const getPageTitle = () => {
  const titles: Record<string, string> = {
    '/about': 'About Us',
    '/cocoa-coffee': 'Coffee, Cocoa & Residues',
    '/electronics': 'Electronics',
    '/decors': 'Decor\'s',
    '/contact': 'Contact Us'
  }
  return titles[route.path] || 'Page'
}

const getPageDescription = () => {
  const descriptions: Record<string, string> = {
    '/about': 'We are a trusted supplier of premium cocoa beans, high-quality coffee (Arabica and Robusta), and cocoa by-products, including cocoa mass, shells, butter, and powder.',
    '/cocoa-coffee': 'We export-import Cameroonian coffee, cocoa beans, cocoa mass, cocoa butter, cocoa powder, and cocoa shells.',
    '/decors': 'We provide wedding planning, elegant decor for weddings and funerals, plus rentals of chairs, canopies, tables, cutlery, flowers, and décor materials.',
    '/electronics': 'We also sell quality electronics, including phones, televisions, phone accessories, woofers, irons, and a wide range of general electronic items.',
    '/contact': 'Looking to place an order, request a quote, or learn more about our cocoa and coffee exports? We\'re here to help. Reach out today and our team will respond promptly.'
  }
  return descriptions[route.path] || 'Welcome to Agri-Management'
}

const getBackgroundImage = () => {
  const images: Record<string, string> = {
    '/about': '/about-us.webp',
    '/cocoa-coffee': '/hero-bg.jpg',
    '/electronics': '/electronic.jpg',
    '/decors': '/decor.jpg',
    '/contact': '/contact.jpg'
  }
  return images[route.path] || '/hero-bg.jpg'
}
</script>


