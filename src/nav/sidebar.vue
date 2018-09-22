<style>
::-webkit-scrollbar {
    width: 0px;  /* remove scrollbar space */
    background: transparent;  /* optional: just make scrollbar invisible */
}
/* optional: show position indicator in red */
::-webkit-scrollbar-thumb {
    background: transparent;  /* optional: just make scrollbar invisible */
}
#sidebar{
    width: 100%;
    background-color: lightblue;
    min-height: 100%;
    position: relative;
}
#sidebar.active{
    margin-left: -200px;
}
</style>
<template>
    <div id="sidebar">
        <div>
            <router-link to="/">Home</router-link>
        </div>
        <div>
            <router-link to="/about">About</router-link>
        </div>
    </div>
</template>
<script>
export default {
    name: 'sidebar',
    data() {
        return{
            isActive:  this.$store.state.sidebaractive
        }
    }
}
</script>

