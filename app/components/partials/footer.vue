<template>
  <footer class="footer -mx-4 md:mx-0">
    <div class="container mx-auto pb-6 flex justify-end">
      <div class="mx-2">
        <div v-html="$md.render(footerText)" class="home__welcome markdown text-right"></div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import settings from '@/content/settings/general.json';

@Component
export default class Footer extends Vue {
  footerText = settings.footerText;
}
</script>

<style lang="scss">
.footer {
  background-color: $orange;
}
</style>
