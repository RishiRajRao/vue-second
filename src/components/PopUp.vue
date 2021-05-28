<template>
  <div>
    <h1>I am popup component</h1>
    <input type="text" v-model="name" name="" id="">
    <button @click="$emit('close',name)">Close Popup</button>
  </div>
</template>

<script>
export default {
name:'PopUp',
emits:['close'],
// this data function is like a state!(for controlled component use this)
data(){
  return{
    name:''
  }
}
}
</script>

<style>

</style>