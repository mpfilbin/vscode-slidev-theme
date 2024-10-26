<script setup lang="ts">
import { computed, useAttrs } from 'vue';

const attrs = useAttrs();
const props = defineProps<{
    src: string;
    height: string;
    width: string;
}>();

const computedSrc = computed(() => `http://localhost:8081/${props.src}`);
</script>

<template>
    <div :class="attrs.class">
        <iframe :src="computedSrc" frameborder="0" :height="height" :width="width"></iframe>
    </div>
</template>