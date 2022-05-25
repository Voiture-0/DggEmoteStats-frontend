<script setup lang="ts">
import TopEmotePosters from '@/components/TopEmotePosters.vue'
import { ref, watchEffect } from 'vue'
import { useRoute, RouterLink } from 'vue-router'

const route = useRoute()

const emoteName = ref(route.params.id as string)

watchEffect(() => {
  emoteName.value = route.params.id as string
})
</script>

<template>
  <main>
    <RouterLink to="/emote/LULW">/emote/LULW</RouterLink>
    <RouterLink to="/emote/MMMM">/emote/MMMM</RouterLink>
    <RouterLink to="/emote/Wowee">/emote/Wowee</RouterLink>
    <RouterLink to="/emote/PepoTurkey">/emote/PepoTurkey</RouterLink>

    {{ emoteName }}

    <TopEmotePosters :emoteName="emoteName" />
  </main>
</template>
