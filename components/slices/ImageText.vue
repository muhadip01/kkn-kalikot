<template>
  <section class="hero">
      <prismic-image class="hero-img" :field="slice.primary.keren_image"/>
      <div class="page-title">
        <prismic-rich-text class="header-page" :field="slice.primary.keren_title"/>
      </div>
  </section>
</template>

<script>
export default {
  props: ['slice'],
  name: 'image-text'
}
</script>

<style scoped>
.hero{
  margin: 20px 0 80px;
  padding: 0em 0px 0;
  background-position: center center;
  background-size: cover;
  position: relative;
} 
.hero-img{
  width: 100%;
  height: 400px
}
.header-page{
  font-size: 4vw;
}
.page-title{
  background: #efdc7c;
  padding: 3em 8em;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: absolute;
  bottom: -60px;
  left: 10px
}
@media (min-width: 768px) {
  .header-page{
    font-size: calc(1vw + 46px);
    margin: 0;
  }
}
@media (max-width: 767px) {
  .hero{
    margin: 20px 0 60px;
    height: 50vh;
    padding: 0;
  }
  .page-title{
    padding: 1em 2em;
    bottom: -30px;
  }
  .header-page{
    font-size: 32px;
    margin: 0;
  }
}
@media (max-width: 381px) {
  .header-page{
    font-size: 24px;
    margin: 0;
  }
  .page-title{
    padding: 1em;
  }
}
</style>