<template>
  <section class='media-sec'>
    <div v-for="item in slice.items" :key="item.id" class="media-item">
        <prismic-link :field="item.media_link" class="medlink">
            <h3>{{ $prismic.asText(item.media_title) }}</h3>
            <prismic-image :field="item.media_image" class="link-img"/>
        </prismic-link>
        <p>klik judul atau gambar diatas untuk mendownload</p>
        <p>{{ $prismic.asText(item.media_description) }}</p>
    </div>
  </section>
</template>

<script>
export default {
  props: ['slice'],
  name: 'media-link'
}
</script>

<style lang="sass" scoped>
.media-sec
    display: flex
    flex-wrap : wrap

.media-item
    width: 28%
    margin-right: 25px

.link-img
    width: 250px
    margin-right: 50px

@media (max-width: 767px)
  .content-section
    margin-bottom: 2rem
  .highlight-left, .highlight-right
    width: 100%
    float: none
    display: block

</style>