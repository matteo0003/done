<script setup lang="ts">
import { fr } from '@nuxt/ui/locale'
import type { NuxtError } from '#app'

defineProps<{
  error: NuxtError
}>()

useSeoMeta({
  title: 'Page not found',
  description: 'We are sorry but this page could not be found.'
})

useHead({
  htmlAttrs: {
    lang: 'fr'
  }
})
</script>

<template>
  <UApp :locale="fr">
    <UError :error="error" />
  </UApp>
</template>
