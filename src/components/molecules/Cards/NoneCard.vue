<template>
  <div class="card" :class="{ 'none-card': noItem }">
    <p v-html="message" />
  </div>
</template>

<script lang="ts" setup>
import { computed } from 'vue'

const props = defineProps<{
  noItem: boolean
}>()

const message = computed(() => props.noItem ? `There's no new <span class="emphasis">task</span> yet 🙂` : `You've done all your <span class="emphasis">tasks</span>!`)
</script>

<style scoped>

</style>