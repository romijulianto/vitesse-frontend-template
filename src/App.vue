<script setup lang="ts">
import { isDark, preferredDark } from '~/common/composables'

useHead({
  title: 'Vitesse Modular NaiveUI',
  meta: [
    { name: 'description', content: 'Opinionated Vite Starter Template with modular architecture design' },
    {
      name: 'theme-color',
      content: computed(() => isDark.value ? '#00aba9' : '#ffffff'),
    },
  ],
  link: [
    {
      rel: 'icon',
      type: 'image/svg+xml',
      href: computed(() => preferredDark.value ? '/favicon-dark.svg' : '/favicon.svg'),
    },
  ],
})

const refMsgTargetEl = ref<any>()
</script>

<template>
  <n-config-provider>
    <n-loading-bar-provider>
      <n-message-provider :to="refMsgTargetEl">
        <n-notification-provider>
          <n-dialog-provider>
            <router-view />
            <div ref="refMsgTargetEl" class="app-msg-target" />
          </n-dialog-provider>
        </n-notification-provider>
      </n-message-provider>
    </n-loading-bar-provider>
  </n-config-provider>
</template>
