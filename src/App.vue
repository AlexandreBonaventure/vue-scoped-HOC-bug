<template>
  <ComponentWithTeleport class="hello" />
  <ComponentRegular class="hello" />
</template>

<script>
import ComponentWithTeleport from './components/ComponentWithTeleport.vue'
import ComponentRegular from './components/ComponentRegular.vue'
import { getCurrentInstance } from 'vue';

export default {
  name: 'App',
  components: {
    ComponentWithTeleport,
    ComponentRegular,
  },
}
</script>

<style lang="postcss" scoped>
.hello {
  color: red;
}
</style>
