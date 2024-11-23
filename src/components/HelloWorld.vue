<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
  <body class="bg-gray-200 h-full w-full">
    <h1>{{ msg }}</h1>
    <h1 class="text-3xl font-bold underline bg-green-500 text-center">
      Hello world! This is a deployment test
    </h1>
    <div class="card text-center m-5">
      <button
        type="button"
        class="m-2 p-2 border-2 border-red-300 bg-red-300 hover:border-red-500 active:bg-red-500 rounded-lg"
        @click="count++"
      >
        count is {{ count }}
      </button>
      <p class="p-2">
        Edit
        <code>components/HelloWorld.vue</code> to test HMR
      </p>
    </div>

    <p class="m-5 text-center">
      Check out
      <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
        >create-vue</a
      >, the official Vue + Vite starter
    </p>
    <p class="m-5 text-center">
      Learn more about IDE Support for Vue in the
      <a
        href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support"
        target="_blank"
        >Vue Docs Scaling up Guide</a
      >.
    </p>
    <p class="m-5 text-[#888] text-center">Click on the Vite and Vue logos to learn more</p>
  </body>
</template>

<style scoped>
/* .read-the-docs {
  color: #888;
} */
</style>
