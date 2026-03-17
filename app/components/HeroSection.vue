<template>
  <section class="relative min-h-screen bg-cover bg-center rounded-br-5xl bg-no-repeat" :style="{ backgroundImage: `url(${backgroundImage})` }">
    <!-- Overlay for better text visibility -->
    <div class="absolute inset-0 bg-black/50"></div>
    
    <!-- Transparent Navbar -->
    <AppHeader class="relative z-10" />
    
    <!-- Hero Content -->
    <div class="relative z-10 flex items-center min-h-screen">
      <div class="w-full max-w-7xl mx-auto px-4">
        <div class="grid lg:grid-cols-2 gap-8 lg:gap-12">
          <!-- Left Side - Title and Description -->
          <div class="text-white space-y-6">
            <h1 class="text-4xl md:text-5xl lg:text-5xl font-semibold leading-tight">
              {{ title }}
            </h1>
            <p class="text-lg md:text-xl leading-relaxed opacity-90">
              {{ description }}
            </p>
            <div v-if="!hideButton" class="pt-8">
              <UButton 
                size="lg" 
                color="primary"
                class="px-8 py-4 text-lg group"
                @click="handlePrimaryAction"
              >
                {{ primaryButtonText }}
                <Icon name="i-heroicons-arrow-right" class="w-5 h-5 ml-2 transition-transform duration-300 group-hover:translate-x-1" />
              </UButton>
            </div>
          </div>

        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
interface Props {
  title?: string
  description?: string
  primaryButtonText?: string
  backgroundImage?: string
  hideButton?: boolean
}

const props = withDefaults(defineProps<Props>(), {
  title: 'Agri-Management: Export-Import Cameroon’s Finest Cocoa & Coffee',
  description: 'We specialize in the export-import of high-quality coffee, cocoa beans, and cocoa residues, including cocoa butter, cocoa mass, cocoa powder, and cocoa shells. All sustainably sourced and expertly processed for international partners.',
  primaryButtonText: 'Learn More',
  hideButton: false
})

const handlePrimaryAction = () => {
  // Navigate to contact or dashboard
  navigateTo('/contact')
}
</script>

<style scoped>
/* Additional styles for the hero section if needed */
</style>
