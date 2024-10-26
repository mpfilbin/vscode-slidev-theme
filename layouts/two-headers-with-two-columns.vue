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
    <div class="grid grid-cols-[repeat(2,1fr)] grid-row-[repeat(2,1fr) w-full h-full" :class="layoutClass">
      <div class="grid-row-start-1 grid-row-end-1 grid-column-start-1 grid-column-end-1 mb-4 h-s">
        <slot name="left-header"/>
      </div>
      <div class="grid-row-start-2 grid-row-end-2 grid-col-start-1 grid-col-end-1 h-md ml-4" :class="props.class">
        <div class="h-full w-full custom-scrollbar overflow-auto">
          <slot name="left"/>
        </div>
      </div>
      <div class="grid-row-start-1 grid-row-end-1 grid-col-start-2 grid-col-end-2 mb-4 h-s">
        <slot name="right-header"/>
      </div>
      <div class="grid-row-start-2 grid-row-end-2 grid-col-start-2 grid-col-end-2 h-md ml-4" :class="props.class">
        <div class="h-full w-full overflow-auto custom-scrollbar">
          <slot name="right"/>
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>

</style>
