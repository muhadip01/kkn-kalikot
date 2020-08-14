<template>
  <div class="homepage">
    <header-prismic/>
    <nuxt />
    <section class="maps">
      <iframe class="gmaps" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d63257.382688964884!2d110.58483939461722!3d-7.727443574051487!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e7a469c17ceea0d%3A0x4027a76e352ecc0!2sKec.%20Kalikotes%2C%20Kabupaten%20Klaten%2C%20Jawa%20Tengah!5e0!3m2!1sid!2sid!4v1597402257024!5m2!1sid!2sid" width="600" height="450" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
    </section>
    <footer-prismic/>
  </div>
</template>

<script>
import HeaderPrismic from '~/components/HeaderPrismic.vue'
import FooterPrismic from '~/components/FooterPrismic.vue'

export default {
  components: {
    HeaderPrismic,
    FooterPrismic
  },
  head () {
    return {
      title: 'Kalkots',
    }
  },
  // Called before rendering the layout (even for error page)
  async middleware({ store, $prismic }) {
    await store.dispatch('fetchMenu', $prismic)
  }
}
</script>
<style>
.maps{
  width:100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.gmaps{
  
  width:1024px;
  margin: 10px auto;
}
</style>