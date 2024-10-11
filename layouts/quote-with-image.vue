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
  <div class="slidev-layout two-cols-header w-full h-full" :class="layoutClass">
    <div class="image" :class="props.class">
      <img :src="image" alt="">
    </div>

    <div class="quote" :class="props.class">
      <p>
        <slot />
      </p>
      <p class="author">
        <em>{{ author }}</em>
      </p>
      
    </div>
  </div>
</template>

<style scoped>
.two-cols-header {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(2, 1fr);
}

.image {
  grid-area: 2 / 1 / 2 / 2;
  @apply h-md;
}

.quote {
  grid-area: 2 / 2 / 2 / 4;
  @apply h-md;
}

.author {
  @apply text-size-sm;
}

</style>