<template>
    <div>
        <h1>Files TODO</h1>
        <div v-for="file in files">
            <h3>{{file.name}}</h3>
            <a v-bind:href="file.location" v-bind:alt="file.location">Download</a>
        </div>
    </div>
</template>

<script>
    import Axios from 'axios'
    export default {
        name: "files",
        created () {
            var _this = this
            Axios.get('https://microsoft111.azurewebsites.net/api/blob').then(
                function(result) {
                    _this.files = result.data
                }
            )
        },
        data () {
        return {
            "files": [{
                "location": "https://microsoft.com",
                "name": "Some random file"
            }]
        }
    }
    }
</script>

<style scoped>

</style>