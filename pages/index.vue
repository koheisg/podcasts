<template lang="pug">
div
  h1 Podcast Activities
  podcast(v-for="(item, index) in feeds" :feed="item" :key="index")
</template>

<style>
@import '//cdn.jsdelivr.net/cal-heatmap/3.3.10/cal-heatmap.css';
@import '//netdna.bootstrapcdn.com/twitter-bootstrap/2.3.2/css/bootstrap-combined.min.css';
</style>

<script>
import axios from 'axios'
import xml2js from '~/lib/xml2js-promise'
import rss from '~/data/rss.json'

export default {
  components: {
    'podcast': require('./podcast.vue').default
  },
  data: function(){
    return rss
  }
}
</script>