<template>
  <ComponentWithAttrs class="hello" />
  <ComponentWithoutAttrs class="hello" />
</template>

<script>
import ComponentWithAttrs from './components/ComponentWithAttrs.vue'
import ComponentWithoutAttrs from './components/ComponentWithoutAttrs.vue'

export default {
  name: 'App',
  components: {
    ComponentWithAttrs,
ComponentWithoutAttrs
  }
}
</script>

<style lang="postcss">
.hello {
  color: red;
}
</style>
