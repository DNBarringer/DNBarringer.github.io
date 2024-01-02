<template>
    <VImg :src="image" alt="Photo" aspect-ratio="1" cover>
        <template v-slot:placeholder>
            <div class="d-flex align-center justify-center fill-height">
                <VProgressCircular
                color="grey-lighten-4"
                indeterminate
                ></VProgressCircular>
            </div>
        </template>
    </VImg>
</template>

<script setup lang="ts">
defineProps<{
  image?: string
}>()
</script>