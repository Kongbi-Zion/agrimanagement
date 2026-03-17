<script setup>
const links = [
  { name: 'Home', path: '/', importantLink: false },
  { name: 'About Us', path: '/about', importantLink: false },
  { name: 'Cocoa & Coffee', path: '/cocoa-coffee', importantLink: true },
  { name: 'Electronics', path: '/electronics', importantLink: true },
  { name: 'Decor\'s', path: '/decors', importantLink: true },
  { name: 'Contact', path: '/contact', importantLink: false }
]

const socialLinks = [
  {
    name: 'Facebook',
    icon: 'i-simple-icons-facebook',
    url: 'https://www.facebook.com/share/1DVz7BL42i'
  },
  {
    name: 'X (Twitter)',
    icon: 'i-simple-icons-x',
    url: 'https://www.linkedin.com/company/106821389/admin/dashboard'
  },
  {
    name: 'LinkedIn',
    icon: 'i-simple-icons-linkedin',
    url: 'https://www.linkedin.com/company/106821389/admin/dashboard'
  }
]
</script>

<template>
  <footer class="bg-secondary text-white">
    <div class="container mx-auto px-4 py-12 sm:py-16 lg:py-24">
      <div class="grid grid-cols-1 sm:grid-cols-1 lg:grid-cols-5 gap-6 sm:gap-8">
        <!-- Company Info -->
        <div class="lg:col-span-2">
          <div class="flex items-center space-x-2 mb-4">
            <Logo/>
          </div>
          <p class="text-white text-sm leading-relaxed lg:max-w-sm">
            We specialize in the export-import of high-quality coffee, cocoa beans, and cocoa residues, including cocoa butter, cocoa mass, cocoa powder, and cocoa shells. All sustainably sourced and expertly processed for international partners.
          </p>
        </div>

        <!-- Quick Links -->
        <div>
          <h3 class="text-lg font-semibold mb-3 sm:mb-4">Quick Links</h3>
          <ul class="space-y-1.5 sm:space-y-2">
            <li v-for="link in links.filter(l => !l.importantLink)" :key="link.name">
              <NuxtLink :to="link.path" class="text-white hover:text-gray-200 transition-colors text-sm">
                {{ link.name }}
              </NuxtLink>
            </li>
          </ul>
        </div>

        <!-- Important Links -->
        <div>
          <h3 class="text-lg font-semibold mb-3 sm:mb-4">Important Links</h3>
          <ul class="space-y-1.5 sm:space-y-2">
            <li v-for="link in links.filter(l => l.importantLink)" :key="link.name">
              <NuxtLink :to="link.path" class="text-white hover:text-gray-200 transition-colors text-sm">
                {{ link.name }}
              </NuxtLink>
            </li>
          </ul>
        </div>

        <!-- Let's Connect -->
        <div>
          <h3 class="text-lg font-semibold mb-3 sm:mb-4">Let's Connect!</h3>
          <p class="text-white text-sm mb-4 leading-relaxed">
            Stay connected with us through our social media pages
          </p>
          <div class="flex space-x-3 sm:space-x-4">
            <NuxtLink
              v-for="social in socialLinks"
              :key="social.name"
              :to="social.url"
              :external="true"
              target="_blank"
              class="text-white hover:text-gray-200 transition-colors p-2 bg-primary md:h-12 md:w-12 h-10 w-10 flex justify-center items-center rounded-full hover:bg-white/10"
              :aria-label="social.name"
            >
              <Icon :name="social.icon" class="md:w-5 md:h-5 w-3.5 h-3.5" />
            </NuxtLink>
          </div>
        </div>
      </div>

      <!-- Bottom Bar -->
      <div class="border-t border-gray-300 mt-8 sm:mt-10 lg:mt-12 pt-6 sm:pt-8">
        <div class="flex flex-col sm:flex-row justify-between items-center gap-4">
          <p class="text-white text-sm text-center sm:text-left">
            © {{ new Date().getFullYear() }} Agri-Management. All rights reserved.
          </p>
          <p class="text-white text-sm text-center sm:text-right">
            Powered by Agri-Management
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>