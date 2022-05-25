<script setup lang="ts">
import { defineProps, watchEffect } from 'vue'

const props = defineProps<{
  emoteName: string
}>()

watchEffect(() => {
  loadData(props.emoteName)
})

function loadData(emoteName: string) {
  console.log(`loading data for '${emoteName}'`)
}
</script>

<template>
  <div>{{ emoteName }}</div>
</template>

<style scoped></style>
