<template>
    <div>
        <h1>Files TODO</h1>
        <div v-for="file in files">
            <h3>{{file.title}}</h3>
            <a v-bind:href="file.url" v-bind:alt="file.filename">Download</a>
            <span>{{file.date}}</span>
        </div>
    </div>
</template>

<script>
    export default {
        name: "files",
        data () {
        return {
            "files": [{
                "filename": "something.jpg",
                "url": "https://microsoft.com",
                "title": "Some random file",
                "date": "2017-03-03"
            },
            {
                "filename": "somethingelse.jpg",
                "url": "https://google.com",
                "title": "Some other file",
                "date": "2017-03-03"
            },
            {
                "filename": "something.jpg",
                "url": "https://github.com/petrepopescu21/quickfrontend",
                "title": "Link to a repo",
                "date": "2017-03-03"
            }]
        }
    }
    }
</script>