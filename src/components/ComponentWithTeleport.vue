<template>
  <teleport :to="to">
    <h1 v-bind="$attrs">This copy should be red as well (scoped with Teleport)</h1>
  </teleport>
</template>

<script>
import { getCurrentInstance } from 'vue';
const ensureElToMountTo = function ensureElToMountTo () {
  const el = document.createElement('div');
  document.body.append(el);
  return el;
};
export default {
  inheritAttrs: false,
  setup() {
    const ctx = getCurrentInstance()
    return {
      to: ensureElToMountTo(),
      scopedId: ctx.vnode.scopeId,
    }
  }
}
</script>
