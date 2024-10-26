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
  <div class="slidev-layout">
    <div class="w-full mb-4 h-s">
      <slot />
    </div>
    <div class="grid grid-cols-1 grid-rows-1 w-full h-full" :class="layoutClass">
      <div class="grid-row-start-1 grid-row-end-1 grid-col-start-1 grid-row-end-1" :class="props.class">
        <div class="h-md ml-4 overflow-auto custom-scrollbar">
          <slot name="body" />
        </div>
      </div>
    </div>
  </div>
</template>

