<template>
    <div class="container">
        <!-- Slice section template -->
        <section v-for="(slice, index) in slices" :key="'slice-' + index">
            <!-- Text slice component -->
            <template v-if="slice.slice_type === 'text_section'">
                <text-slice :slice="slice"/>
            </template>
            <!-- Quote slice component -->
            <template v-else-if="slice.slice_type === 'quote'">
                <quote-slice :slice="slice"/>
            </template>
            <!-- Full Width Image slice component -->
            <template v-else-if="slice.slice_type === 'full_width_image'">
                <full-width-image :slice="slice"/>
            </template>
            <!-- Image Gallery slice component -->
            <template v-else-if="slice.slice_type === 'image_gallery'">
                <image-gallery :slice="slice"/>
            </template>
            <!-- Image Highlight slice component -->
            <template v-else-if="slice.slice_type === 'image_highlight'">
                <image-highlight :slice="slice"/>
            </template>
            <!-- Embed video slice component -->
            <template v-else-if="slice.slice_type === 'embed_video'">
                <video-slice :slice="slice"/>
            </template>
            <!-- media link slice component -->
            <template v-else-if="slice.slice_type === 'media'">
                <media-link :slice="slice"/>
            </template>
            <!-- single media link slice component -->
            <template v-else-if="slice.slice_type === 'single-media'">
                <single-media :slice="slice"/>
            </template>
            <!-- image text keren link slice component -->
            <template v-else-if="slice.slice_type === 'image_text'">
                <image-text :slice="slice"/>
            </template>
        </section>
    </div>
</template>

<script>
// Imports for all slices
const TextSlice = () => import("./slices/TextSlice.vue");
const QuoteSlice = () => import("./slices/QuoteSlice.vue");
const FullWidthImage = () => import("./slices/FullWidthImage.vue");
const ImageGallery = () => import("./slices/ImageGallery.vue");
const ImageHighlight = () => import("./slices/ImageHighlight.vue");
const VideoSlice = () => import("./slices/VideoSlice.vue");
const MediaLink = () => import("./slices/MediaLink.vue");
const SingleMedia = () => import("./slices/SingleMedia.vue");
const ImageText = () => import("./slices/ImageText.vue");

export default {
  props: ['slices'],
  name: 'slices-block',
  components: {
    TextSlice,
    QuoteSlice,
    FullWidthImage,
    ImageGallery,
    ImageHighlight,
    VideoSlice,
    MediaLink,
    SingleMedia,
    ImageText,
  },
}
</script>