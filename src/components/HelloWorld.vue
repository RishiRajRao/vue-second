<template>
  <div class="hello">
    <h1>{{ msg }} {{goal}}</h1>
    <Provide_inject/>
  </div>
</template>

<script>
import Provide_inject from './Provide_inject.vue'
export default {
  name: 'HelloWorld',
  components:{
    Provide_inject
  },
  // props: ['msg']
 
   props:{
    msg:String,
    goal:String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
