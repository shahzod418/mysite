<script setup lang="ts">
import { TELEGRAM_LINK, VK_LINK, GITHUB_LINK } from '~/constants/links';
import { GITHUB_TITLE } from '~/constants/title';

const { t } = useI18n();
</script>

<template>
  <div class="flex h-14 border-t border-line">
    <div
      class="flex h-full grow items-center border-r border-line px-5 md:grow-0"
    >
      <span class="text-label text-secondary">{{ t('findMe') }}</span>
    </div>
    <LayoutLink
      :to="TELEGRAM_LINK"
      class="group/telegram w-14 border-r"
      target="_blank"
    >
      <IconTelegram
        class="btn-social transition group-hover/telegram:opacity-100"
      />
    </LayoutLink>
    <LayoutLink :to="VK_LINK" class="group/vk w-14 border-r" target="_blank">
      <IconVk class="btn-social transition group-hover/vk:opacity-100" />
    </LayoutLink>
    <LayoutLink
      :to="GITHUB_LINK"
      class="group/github w-14 md:ml-auto md:w-auto md:border-l md:px-8"
      target="_blank"
    >
      <IconGithub
        class="btn-social transition group-hover/github:opacity-100 md:hidden"
      />
      <div
        class="hidden h-full items-center group-hover/github:underline md:flex"
      >
        <span>{{ GITHUB_TITLE }}</span>
        <IconGithub class="btn-social ml-1 opacity-100" />
      </div>
    </LayoutLink>
  </div>
</template>
