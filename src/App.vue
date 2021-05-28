<template>
  <div>
    <!-- <button @click="showPopUp = true">Open PopUp</button>
    <PopUp v-show="showPopUp" @close="closePopUp"/> -->

    <button @click="showMe" name="tabA">TabA</button>
    <button @click="showMe" name="tabB">TabB</button>
    <button @click="showMe" name="tabC">TabC</button>
    <h1>{{family.name}}</h1>
    <TabA v-show="showA"/>
    <TabB v-show="showB"/>
    <TabC v-show="showC"/>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
// import PopUp from './components/PopUp.vue'
import TabA from "./components/TabA.vue";
import TabB from "./components/TabB.vue";
import TabC from "./components/TabC.vue";

export default {
  name: "App",
  components: {
    //  HelloWorld
    // PopUp
    TabA,
    TabB,
    TabC,
  },
  data() {
    return {
      // myGoal: "love your job",
      // success: "love your work",
      // name: "Ashish",
      // showPopUp: false,

      showA: true,
      showB: false,
      showC: false,
      family:{name:'rishi',home:'bellandur'}
      
    };
  },

  methods: {
    // closePopUp(val) {
    //   this.showPopUp = false;
    //   alert(val);
    // },

    showMe(event){
      alert('i am called');
      if(event.target.name == 'tabA'){
        this.showA=true;
        this.showB=false;
        this.showC=false;
      }
      if(event.target.name=='tabB'){
        this.showA=false;
        this.showB=true;
        this.showC=false;
      }
      if(event.target.name=='tabC'){
        this.showA=false;
        this.showB=false;
        this.showC=true;
      }
    }
  },
  // provide is used for the passing global data to all decendent components but when used in the same component use 'provide' function and return
  // provide:{
  //   UserName:'RishiNI'
  // }

  // provide() {
  //   return {
  //     userName: this.name,
  //   };
  // }
};

// try to use shorthand for helloworld
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
