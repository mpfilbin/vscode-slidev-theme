<script setup lang="ts">
const props = defineProps({
    class: {
      type: String,
    },
    layoutClass: {
      type: String,
    },
    image: {
      type: String,
    },
    author: {
      type: String,
    }
  })
</script>

<template>
  <div class="slidev-layout">
    <div class="grid grid-cols-2 grid-row-1 w-full h-full" :class="layoutClass">
      <div class="grid-row-start-1 grid-row-end-1 grid-col-start-1 grid-col-end-1" :class="props.class">
        <img :src="image" alt="">
      </div>

      <div class="grid-row-start-1 grid-row-end-1 grid-col-start-2 grid-col-end-2" :class="props.class">
        <p>
          <slot />
        </p>
        <p class="text-size-sm">
          <em>{{ author }}</em>
        </p>

      </div>
    </div>
  </div>
</template>
