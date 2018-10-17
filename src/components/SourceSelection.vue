<template>
    <div class="sourceselection">
        <h4>Select News Source</h4>
        <select class="form-control" v-on:="sourceChanged">
            <option 
            v-bind:value="source.id" 
            v-for="(source, i) in sources" :key="i">{{source.name}}</option>
        </select>
    </div>    
</template>

<script>
export default {
    name: 'sourceselection',
    data() {
        return {
            sources: [],
            source: ''
        }
    },
    methods: {
        sourceChanged: function(e) {
            for (var i = 0; i < this.sources.lenght; i++) {
                if (this.sources[i].id == e.tarhet.value) {
                    this.source = this.source[i];
                }
            }
        }
    },
    created: function() {
        this.$http.get('https://newsapi.org/v2/sources?&apiKey=4370ceb1a6fe4e1ba693a36ce793609b')
            .then(response => {
                this.sources = response.data.sources
            })
    }
}
</script>

<style scoped>

</style>


