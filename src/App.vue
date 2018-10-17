<template>
  <div id="app" class="container">
    <SourceSelection v-on:sourceChanged="sourceChanged" />
    <NewsList v-bind:source="source" />
  </div>
</template>

<script>
import SourceSelection from './components/SourceSelection'
import NewsList from './components/NewsList'

export default {
  name: 'App',
  components: {
    SourceSelection,
    NewsList
  },
   data () {
     return {
       source: ''
     }
   },
   methods: {
     sourceChanged: function (source) {
       this.source = source;
     }
   }
}
</script>

<style>
#app {
  text-align: center;
}
</style>
