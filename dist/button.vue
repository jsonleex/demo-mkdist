<script lang="ts">
export const size: ButtonProps['size'][] = ['small', 'large']
</script>

<script setup lang="ts">
export interface ButtonProps {
  size: 'small' | 'large'
}

defineProps<ButtonProps>()
</script>

<template>
  <button :class="['x-button', size && `x-button-${size}`]">
    <slot />
  </button>
</template>

<style>
@import url('./button.css');
</style>