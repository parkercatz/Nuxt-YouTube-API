<template>
  <div class="d-flex flex-column justify-start align-centar fluid">
    <v-container>
      <h1>{{ title }}</h1>
      <p>{{ description }}</p>
      <v-row class="align-start justify-start">
        <v-col
          v-for="video in videos"
          :key="video.snippet.resourceId.videoId"
          cols="12"
          md="4"
        >
          <iframe
            :src="`https://www.youtube.com/embed/${video.snippet.resourceId.videoId}`"
            frameborder="0"
          ></iframe>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  props: {
    videos,
  },
  data() {
    return {
      title: 'Videos',
      description: 'My PlayList Videos',
    }
  },
}
</script>

<style lang="scss" scoped></style>
