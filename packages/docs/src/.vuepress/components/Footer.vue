<template>
  <div class="footer">
    {{ text[language].prefix }} <a :href="text[language].link" target="_blank" rel="noopener">Bazzite</a>.
    <br>
    {{ text[language].copyright }}
  </div>
</template>

<script>
export default {
  data: () => ({
    text: {
      en: {
        prefix: 'Made with ❤️ by',
        link: 'https://www.bazzite.com?ref=statusfy-docs',
        copyright: 'Copyright © 2019 Bazzite, LLC. All Rights Reserved.'
      },
      es: {
        prefix: 'Hecho con ❤️ por',
        link: 'https://www.bazzite.com/es/?ref=statusfy-docs',
        copyright: 'Copyright © 2019 Bazzite, LLC. Todos los derechos reservados.'
      }
    }
  }),
  computed: {
    language() {
      return this.$lang.split('-')[0];
    }
  }
}
</script>
