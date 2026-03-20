<template>
  <header class="absolute w-full max-w-7xl pt-7 mx-auto top-0 left-0 right-0 z-50">
    <div class="container mx-auto px-4">
      <div class="flex justify-between items-center h-16">
        <NuxtLink to="/" class="flex items-center space-x-2">
          <Logo/>
        </NuxtLink>
        <nav class="hidden md:flex items-center space-x-8">
          <NuxtLink
            v-for="link in links"
            :key="link.name"
            :to="link.path"
            class="text-white font-light hover:text-gray-200 transition-colors"
            :class="{ 'text-green-300 font-light': $route.path === link.path }"
          >
            {{ link.name }}
          </NuxtLink>
        </nav>
        <div class="lg:hidden aspect-square flex justify-center items-center bg-primary">
          <UButton
            color="neutral"
            variant="ghost"
            size="sm"
            class="text-white bg-transparent hover:bg-transparent"
            @click="toggleMobileMenu"
          >
            <Icon name="i-heroicons-bars-3" class="w-5 h-5" />
          </UButton>
        </div>
      </div>
      <div 
        v-if="showMobileMenu" 
        class="fixed inset-0 z-50 md:hidden"
        @click="closeMobileMenu"
      >
        <div 
          class="fixed left-0 right-0 shadow-5xl rounded-t-3xl bottom-0 h-fit bg-white transform transition-transform duration-300"
          :class="{ 'translate-y-0': showMobileMenu, 'translate-y-full': !showMobileMenu }"
          @click.stop
        >
          <div class="p-6">
            <nav class="flex flex-col space-y-4">
              <NuxtLink
                v-for="link in links"
                :key="link.name"
                :to="link.path"
                class="text-gray-700 hover:text-gray-900 transition-colors py-2"
                @click="closeMobileMenu"
              >
                {{ link.name }}
              </NuxtLink>
            </nav>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
const links = [
  { name: 'Home', path: '/', importantLink: false },
  { name: 'About Us', path: '/about', importantLink: false },
  { name: 'Cocoa & Coffee', path: '/cocoa-coffee', importantLink: true },
  { name: 'Decor\'s', path: '/decors', importantLink: true },
  { name: 'Electronics', path: '/electronics', importantLink: true },
  { name: 'Contact', path: '/contact', importantLink: false }
]

const showMobileMenu = ref(false)

const toggleMobileMenu = () => {
  showMobileMenu.value = !showMobileMenu.value
}

const closeMobileMenu = () => {
  showMobileMenu.value = false
}

const route = useRoute()
watch(() => route.path, () => {
  showMobileMenu.value = false
})
</script>
