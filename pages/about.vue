<template>
  <div>
    <VCard>
      <VCardTitle>
        <span class="text-3xl">【魯尼按鈕】</span>
      </VCardTitle>
      <VCardText class="text-lg">
        <ul class="list-disc pl-6">
          <li>製作:
            <span v-for="(author, i) in site.footer.authors" :key="i">
              <a class="link" :href="author.link" target="_blank">{{ author.name }}</a>
              <span v-if="i !== site.footer.authors.length - 1">、</span>
            </span>
          </li>
          <li>音檔素材來源: YT剪輯、Twitch Clip、哈士祈 Discord 音效板、月司</li>
          <li>圖檔素材來源: <a class="link" href="https://lit.link/en/yuuminekone" target="_blank">憂瀰*yuumi</a></li>
        </ul>
      </VCardText>
    </VCard>
  </div>
</template>
<script setup lang="ts">
import site from '@/assets/locales/site.json'
</script>

<style scoped>
.link {
  @apply text-primary-500 underline;
}

ul * {
  @apply text-lg;
}
</style>
