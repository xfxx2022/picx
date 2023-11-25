<template>
  <div class="page-container feedback-page-container">
    <div class="help-info-item description">🏞️ {{ $t('feedback.text_1') }}</div>

    <div class="help-info-item">
      🌍 {{ $t('feedback.text_2') }} {{ $t('shortcut_key') }}：<code>{{ shortcutKey }}</code>
    </div>

    <div class="help-info-item" style="margin-bottom: 2rem">🎁 {{ $t('feedback.text_3') }}</div>

  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import { getOSName } from '@/utils'

const shortcutKey = computed(() => (getOSName() === 'win' ? 'Ctrl + D' : 'Command + D'))
</script>

<style scoped lang="stylus">
@import "./feedback-info.styl"
</style>
