<template>
  <section class='highlight content-section'>
    <div class="highlight-left">
      <prismic-image :field="slice.primary.featured_image"/>
    </div>
    <div class="highlight-right">
      <prismic-rich-text :field="slice.primary.title"/>
      <prismic-rich-text :field="slice.primary.headline"/>
      <p>
        <prismic-link :field="slice.primary.link">{{ $prismic.asText(slice.primary.link_label) }}</prismic-link>
      </p>
    </div>
  </section>
</template>

<script>
export default {
  props: ['slice'],
  name: 'image-highlight'
}
</script>

<style lang="sass" scoped>
.highlight
  position: relative
  overflow: auto

.highlight-left
  width: 20%
  float: left
  height: 250px

.highlight-right
  width: 78%
  float: right

@media (max-width: 767px)
  .content-section
    margin-bottom: 2rem
  .highlight-left, .highlight-right
    width: 100%
    float: none
</style>

