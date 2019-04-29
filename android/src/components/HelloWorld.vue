<template>
  <div class="hello">
   <button @click="getPoem">获取推荐</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{
    getPoem:function(){
      var url = "https://api.apiopen.top/recommendPoetry";
      var url2 = "https://api.apiopen.top/searchAuthors?name=李白";
      var that = this;
      this.axios.get(url).then(function(result){
        console.log(result.data);
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
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
