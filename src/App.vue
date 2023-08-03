<template>
    <HelloWorld />

    <ScrollTrigger2 />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

import ScrollTrigger2 from "./components/ScrollTrigger2.vue";

export default {
    name: "App",
    components: {
        HelloWorld,

        ScrollTrigger2,
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}
</style>
