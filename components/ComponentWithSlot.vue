<template>
  <div>
    <Transition name="fade">
      <slot v-if="!isLoading" name="theSlot"></slot>
    </Transition>
  </div>
</template>

<script setup lang="ts">
  defineProps<{
    isLoading: boolean;
  }>();
</script>
