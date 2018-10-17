<template>
  <div id="app" class="container">
    <SourceSelection />
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
   }
}
</script>

<style>
#app {
  text-align: center;
}
</style>
