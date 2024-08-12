<template>
  <Cube />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Cube from './components/Cube.vue'

export default defineComponent({
  name: 'App',
  components: {
    Cube,
  },
});
</script>