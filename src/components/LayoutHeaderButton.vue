<script>
import { ref } from 'vue'

export default {
  props: {
    text: String,
    link: String,
  }
}
</script>

<template>
  <button class="group">
    <a :href=link class="capitalize font-semibold text-lg"> {{ text }} </a>
    <div class="bg-stone-800 w-0 group-hover:w-full h-0.5 duration-200"></div>
  </button>
</template>