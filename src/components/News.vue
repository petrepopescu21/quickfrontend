<template>
  <div class="hello">
    <h1>News</h1>
    <div v-for="article in news">
        <h3>{{article.title}}</h3>
        <span>{{article.date}}</span>
        <p>{{article.body}}</p>
      </div>

  </div>
</template>

<script>
export default {
  name: 'news',
  data () {
    return {
      news: [{
        "title": "First piece of news",
        "date": "2017-05-03",
        "body": "Bla bla bla"
      },
      {
        "title": "Second piece of news",
        "date": "2017-05-02",
        "body": "Bla bla bla blah!"
      },
      {
        "title": "Old piece of news",
        "date": "2016-05-03",
        "body": "Bla bla bla blargh!"
      }]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
