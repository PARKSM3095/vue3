<template>
  <header>
    <nav class="menu">
      <a v-for="(nav,i) in menu" :key="i">{{ nav }}</a>
    </nav>
  </header>
  <div v-for="(a,i) in products" :key="i">
    <h4>{{ a }}</h4>
    <p>{{ price[i] }} 만원</p>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      menu : ['Home','Products','About'],
      products : ['역삼동원룸','천호동원룸','마포구원룸'],
      price : [50,100,150]
    }
  },
  components: {

  }
}
</script>

<style>
body{
  margin:0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.menu{
  background:darkslateblue;
  padding:15px;
}
.menu a{
  color:#fff;
  padding: 0 10px;
}
</style>
