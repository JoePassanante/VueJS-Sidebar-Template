<template>
  <div id="app">
  <div id = "top">
    testing
  </div>
    <div id="leftCol">
          <sidebar></sidebar>
    </div>
    <div id="content"> 
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
  data() {
    return {
      margin: 200
    };
  },
  mounted: function() {
    
  }
};
</script>
<style>
.app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}
#nav {
  padding: 30px;
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
}
</style>
