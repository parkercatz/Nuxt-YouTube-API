<template>
  <div class="d-flex flex-column justify-start align-centar fluid">
    <v-container>
      <h1>{{ title }}</h1>
      <p>{{ description }}</p>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Videos',
      description: 'My PlayList Videos',
    }
  },
}
</script>

<style lang="scss" scoped></style>
