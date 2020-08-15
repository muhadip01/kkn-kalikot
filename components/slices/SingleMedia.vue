<template>
  <section class='solmed-sec'>
    <div class="solmed-item">
        <prismic-link :field="slice.primary.solmed_link" class="solmedlink">
            <h3>{{ $prismic.asText(slice.primary.solmed_title) }}</h3>
            <prismic-image :field="slice.primary.solmed_image" class="solmed-img"/>
        </prismic-link>
        <p>klik judul atau gambar diatas untuk mendownload</p>
        <p>{{ $prismic.asText(slice.primary.solmed_description) }}</p>
    </div>
  </section>
</template>

<script>
export default {
  props: ['slice'],
  name: 'single-media'
}
</script>

<style lang="sass" scoped>
@media (max-width: 767px)
  .content-section
    margin-bottom: 2rem
</style>