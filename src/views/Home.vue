<template>
  <div class="home">
    <img @mouseleave="mouseOut" @mouseover="mouseOver" alt="Vue logo" src="../assets/logo.png">
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
        mouseOver: function(){
          console.log("yas")
            this.$store.state.sidebaractive = true
          
        },
        mouseOut:function(){
          console.log("Out")
          this.$store.state.sidebaractive = false
        }
    }
}
</script>
