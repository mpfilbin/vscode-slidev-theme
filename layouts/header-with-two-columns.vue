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
    <div class="grid grid-cols-[repeat(2,1fr)] grid-rows-1 w-full h-full" :class="layoutClass">
      <div class="grid-row-start-1 grid-row-end-2 grid-column-start-1 grid-column-end-2 h-md ml-4" :class="props.class">
        <div class="h-full w-full overflow-auto custom-scrollbar">
          <slot name="left" />
        </div>
      </div>
      <div class="grid-row-start-1 grid-row-end-2 grid-column-start-2 ml-4" :class="props.class">
        <div class="h-full w-full overflow-auto custom-scrollbar">
          <slot name="right" />
        </div>
      </div>
    </div>
  </div>
</template>
