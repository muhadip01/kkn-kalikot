<template>
  <section class='solmed-sec'>
    <div class="solmed-item">
        <prismic-link :field="slice.primary.solmed_link" class="solmedlink">
            <h3 class="solmed-ttl">{{ $prismic.asText(slice.primary.solmed_title) }}</h3>
            <prismic-image :field="slice.primary.solmed_image" class="solmed-img"/>
        </prismic-link>
        <p class="solmed-dl">klik judul atau gambar diatas untuk mendownload</p>
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

.solmed-img
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 30%;

.solmed-ttl
    text-align: center

.solmed-dl
    text-align: center

@media (max-width: 767px)
  .content-section
    margin-bottom: 2rem
</style>