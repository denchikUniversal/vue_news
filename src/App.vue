<template>
  <div id="app" class="container">
    <SourceSelection />
    <NewsList />
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
  }
}
</script>

<style>
#app {
  text-align: center;
}
</style>
