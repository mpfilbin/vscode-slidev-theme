<!--
  Usage:
```md
---
layout: two-cols-header
---
This spans both
::left::
# Left
This shows on the left
::right::
# Right
This shows on the right
::bottom::
This shows at the bottom, aligned to the end (bottom) of the grid
```
-->

<script setup lang="ts">
const props = defineProps({
  class: {
    type: String,
  },
  layoutClass: {
    type: String,
  },
})
</script>

<template>
  <div class="slidev-layout two-cols-header w-full h-full" :class="layoutClass">
    <div class="col-header">
      <slot />
    </div>
    <div class="col-body" :class="props.class">
      <div class="h-full w-full overflow-auto custom-scrollbar">
        <slot name="body" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.two-cols-header {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  grid-template-rows: repeat(2, 1fr);
}

.col-header {
  grid-area: 1 / 1 / 1 / 1;
  @apply mb-4 h-s;
}
.col-body {
  grid-area: 2 / 1 / 2 / 1;
  @apply h-md ml-4;
}

.custom-scrollbar::-webkit-scrollbar {
  width: 0;
  height: 0;
}
.custom-scrollbar {
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}
</style>