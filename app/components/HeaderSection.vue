<template>
  <section class="relative rounded-br-[2.5rem] md:rounded-br-[8.5rem] min-h-[calc(100vh-350px)] md:min-h-[calc(100vh-600px)] bg-cover bg-center bg-no-repeat" :style="{ backgroundImage: `url(${backgroundImage})` }">
    <div class="absolute inset-0 bg-black/50 rounded-br-[2.5rem] md:rounded-br-[8.5rem]"></div>
    
    <AppHeader class="relative z-10" />
    
    <div class="relative z-10 flex items-center min-h-[calc(100vh-350px)] md:min-h-[calc(100vh-600px)]">
      <div class="w-full max-w-7xl mx-auto max-md:px-4">
        <div class="grid lg:grid-cols-2 gap-8 lg:gap-12">
          <div class="text-white space-y-6">
            <h1 class="text-3xl lg:text-5xl font-semibold leading-tight">
              {{ title }}
            </h1>
            <p class="md:text-lg font-light leading-relaxed opacity-90">
              {{ description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
interface Props {
  title: string
  description: string
  backgroundImage: string
}

const props = defineProps<Props>()
</script>
