<script setup lang="ts">
import { APP_TITLE } from '~/constants/title';

useHead({
  title: APP_TITLE,
  meta: [
    { name: 'description', content: 'Frontend Developer Davlatov Shahzod' },
  ],
  link: [{ rel: 'icon', type: 'image/svg+xml', href: '/box.svg' }],
});
</script>

<template>
  <Body class="bg-background">
    <Base id="test" />
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </Body>
</template>
