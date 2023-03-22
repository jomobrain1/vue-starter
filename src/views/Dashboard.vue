<template>
  <div
    class="w-full dash items-center font-bold text-white flex justify-center text-xl bg-blue-300"
  >

    <h1>
      Dashboard <b>{{ test }}</b>
    </h1>
  </div>
</template>

<script setup>
import { computed } from "vue";
import store from "../store";

const test = computed(() => store.state.test);
</script>

<style scoped>
.dash {
  height: 100vh;
}
</style>
