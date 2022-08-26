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
  <a :href=link class="group cursor-pointer">
    <p class="capitalize font-semibold text-lg"> {{ text }} </p>
    <div class="bg-stone-800 w-0 group-hover:w-full h-0.5 duration-200"></div>
  </a>
</template>