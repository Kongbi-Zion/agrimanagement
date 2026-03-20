<template>
  <NuxtLink 
    :to="to"
    :class="[
      'inline-flex items-center px-8 py-4 text-[14px] font-medium rounded-lg transition-colors group shadow-lg',
      variant === 'primary' ? 'bg-primary text-white hover:bg-primary/90' : '',
      variant === 'secondary' ? 'bg-secondary text-white hover:bg-secondary/90' : '',
      customClass
    ]"
  >
    {{ text }}
    <Icon 
      name="i-heroicons-arrow-right" 
      :class="[
        'w-4 h-4 ml-2 transition-transform duration-300',
        iconHoverClass
      ]" 
    />
  </NuxtLink>
</template>

<script setup lang="ts">
interface Props {
  to: string
  text: string
  variant?: 'primary' | 'secondary'
  iconHoverClass?: string
  customClass?: string
}

withDefaults(defineProps<Props>(), {
  variant: 'primary',
  iconHoverClass: 'group-hover:translate-x-1'
})
</script>
