<template>
  <div class="home">
    <img @click="mouseClick" alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
export default {
  name: 'home',
  components: {
    HelloWorld
  },
   methods: {
        mouseClick: function(){
          console.log("yas")
            this.$store.state.sidebaractive =  !this.$store.state.sidebaractive 
        },
    }
}
</script>
