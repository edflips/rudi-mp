<template>
  <figure>
    <figcaption class="sr-only">{{ title }}</figcaption>
    <vue-plyr>
      <audio>
        <source :src="require(`@/assets/audio/${audio}`)" type="audio/mp4" />
      </audio>
    </vue-plyr>
  </figure>
</template>

<script>
export default {
  name: 'AudioPlayer',
  props: {
    title: {
      type: String,
      required: true,
    },
    audio: {
      type: String,
      required: true,
    },
  },
}
</script>

<style></style>
