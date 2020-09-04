<template>
<!-- skjdhfkjh -->
  <h1>Scope: {{scopedId}} This copy should be red</h1>
</template>

<script>
import { getCurrentInstance } from 'vue';

export default {
  // inheritAttrs: false,
  setup() {
    const ctx = getCurrentInstance()
    return {
      scopedId: ctx.vnode.scopeId,
    }
  }
}
</script>
