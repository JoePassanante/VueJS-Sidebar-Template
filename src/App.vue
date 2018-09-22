<template>
  <div id="app">
  <div id = "top">
     <b-button @click="mouseClick" variant="primary">
                Do your Thing
            </b-button>
  </div>
    <div id="leftCol" v-bind:class="{ active: this.$store.state.sidebaractive}">
          <sidebar></sidebar>
    </div>
    <div id="content"  v-bind:class="{ active: this.$store.state.sidebaractive}"> 
        <router-view/>
    </div>
  </div>
</template>
<script>
import Sidebar from "@/nav/sidebar.vue";
export default {
  components: {
    Sidebar
  },
  mounted: function() {

  },
     methods: {
        mouseClick: function(){
          console.log("yas")
            this.$store.state.sidebaractive =  !this.$store.state.sidebaractive 
        },
    }
};
</script>
<style>

.app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}
#top {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 999;
  width: 100%;
  height: 40px;
  background: #2f353a;
}
#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
#leftCol {
  /* No idea Why we need to set in negetive. There is no padding. It makes no sense.  */
  margin-left:-8px; 
  margin-top: 40px;
  position: fixed;
  width: 200px;
  background-color: #ddd;
  font-size: 21px;
  overflow-y: scroll;
  top: 0;
  bottom: 0;
}

#content {
  margin-top: 40px;
  position: relative;
  margin-left: 200px;
  -webkit-transition: margin-left 0.2s; /* For Safari 3.1 to 6.0 */
  transition: margin-left 0.2s;
}

#content.active{
    margin-left: 0px;
}
#leftCol{
    margin-left:0px;
    -webkit-transition: margin-left 0.2s; /* For Safari 3.1 to 6.0 */
    transition: margin-left 0.2s;
}
#leftCol.active{
    margin-left: -200px;
}
</style>
