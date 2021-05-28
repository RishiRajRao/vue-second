<template>
  <div>
    This is test for global data transfer:{{userName}}
    <h1>My name is {{name}}</h1>
    </div>
</template>

<script>

export default {
name:'Provide_inject',
data(){
return{
  name:'Rahul'
}
},
inject:['userName']
}
</script>

<style scoped>

</style>