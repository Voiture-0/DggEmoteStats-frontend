<script setup lang="ts">
import TheWelcome from '@/components/TheWelcome.vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const emoteId = parseInt(route.params.id as string)
</script>

<template>
  <main>
    {{ $route.params.id }}
    {{ emoteId }}
  </main>
</template>
