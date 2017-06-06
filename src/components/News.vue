<template>
  <div class="hello">
    <h1>News</h1>
    <div v-for="article in news">
        <h3>{{article.title}}</h3>
        <span>{{article.data}}</span>
        <p>{{article.body}}</p>
      </div>

  </div>
</template>

<script>
import Axios from 'axios'
export default {
  name: 'news',
  created () {
    var _this = this
      Axios.get('https://microsoft111.azurewebsites.net/api/table').then(
        function(result){
          console.log(result.data)
          _this.news = result.data
        }
      )
  },
  data () {
    return {
      news: [{
        "title": "News is still loading",
        "data": "2017-05-03",
        "body": "Bla bla bla"
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
