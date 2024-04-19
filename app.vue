<template>
  <div>
    <ComponentWithSlot :isLoading="pending">
      <template #theSlot>
        Hi, I'm slotted content!
      </template>
    </ComponentWithSlot>
  </div>
</template>

<script setup>
  const { pending } = await useFetch('https://dummyjson.com/products/1');
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>