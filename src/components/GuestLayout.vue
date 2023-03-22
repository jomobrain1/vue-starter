<template>
  <div
    class="bg-green-400 h-screen overflow-hidden flex items-center justify-center"
  >
    <div class="bg-white lg:w-5/12 md:6/12 w-10/12 shadow-3xl">
      <div class="flex justify-center text-xl">
        <h1 class="text-center mt-10 text-bold">{{ title }}</h1>
      </div>
      <form class="px-12 py-10" @submit.prevent="emit('submitForm')" method="POST">
        <slot></slot>
      </form>
    </div>
  </div>
</template>

<script setup>
const { title } = defineProps({
  title: String,
});

const emit=defineEmits(['submitForm'])

</script>

<style></style>
