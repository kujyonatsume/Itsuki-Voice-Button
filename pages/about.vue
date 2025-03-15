<template>
  <div>
    <VCard>
      <VCardTitle>
        <span class="text-3xl">【玥玥按鈕】</span>
      </VCardTitle>
      <VCardText class="text-lg">
        <ul class="list-disc pl-6">
          <li>製作:
            <span v-for="(author, i) in site.footer.authors" :key="i">
              <a class="link" :href="author.link" target="_blank">{{ author.name }}</a>
              <span v-if="i !== site.footer.authors.length - 1">、</span>
            </span>
          </li>
          <li>協作: 珞鳶</li>
          <li>音檔素材來源: 珞鳶、奈良</li>
          <li>圖檔素材來源: 珞鳶</li>
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
