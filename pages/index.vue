<template>
  <div class="container flex flex-col mx-auto mt-16">
    <article
      v-for="show in shows"
      :key="show.title"
      class="p-8 mx-2 bg-white rounded shadow"
    >
      <h1 class="mb-4 text-xl">
        {{ show.title }}
      </h1>
      <AudioPlayer :title="show.title" :audio="show.audio" />
    </article>
  </div>
</template>

<script>
import AudioPlayer from '~/components/AudioPlayer.vue'

export default {
  components: {
    AudioPlayer,
  },
  data() {
    return {
      shows: [
        {
          title: 'JellyCat Radio - Episode 1: 2nd May 2020',
          audio: '01-JellyCat-Radio-Episode-1-2nd-May-2020.m4a',
        },
      ],
    }
  },
}
</script>

<style></style>
