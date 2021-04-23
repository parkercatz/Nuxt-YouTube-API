<template>
  <Video :videos="videos" />
</template>

<script>
import axios from 'axios'
export default {
  async asyncData() {
    const playlistId = 'PLou3zjMo7ZedWTV_ZY8ZwbILgxbW-SSBE'
    const part = 'snippet'
    const baseUrl = `https://youtube.googleapis.com/youtube/v3/playlists?part=${part}&key=${playlistId}`
    const results = await axios
      .get(baseUrl)
      .then((result) => {
        return result.data.items
      })
      .catch(() => {})
    return {
      videos: results,
    }
  },
}
</script>
