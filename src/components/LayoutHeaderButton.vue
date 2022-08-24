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
    <p class="capitalize"> {{text}} </p>
</template>