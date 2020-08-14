<template>
  <div class="bg">
    <footer class="footer">
     <div class="foothead">
        <nuxt-link to="/" class="logo">
          <prismic-image :field="$store.state.menu.image"/>
        </nuxt-link>
      <h2>Kecamatan Kalikotes</h2>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'FooterPrismic'
}
</script>

<style lang="sass" scoped>
.footer
  padding: 40px 0
  margin: 0 auto
  text-align: center
  border-top: 1px solid

.bg
  width: calc(100% + 40px)
  background: #b3fff5
  margin: 0 -20px -20px

.logo
  width: 100px
</style>
