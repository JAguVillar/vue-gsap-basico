<template>
    <div class="maincito">
        <div class="prueba" ref="prueba"></div>
    </div>
</template>

 <script>
import { gsap } from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);
export default {
    name: "ScrollTrigger",
    data() {
        return {
            text: "Hello World",
        };
    },
    mounted() {
        //  let myDiv = this.$refs.prueba;
        gsap.to(".prueba", {
            scrollTrigger: {
                trigger: ".maincito",
                pin: true,
                markers: true,
            },
            x: 500,
            duration: 1,
        });
    },
    methods: {},
};
</script> 

<style scoped>
.maincito {
    height: 100vh;
    background: salmon;
    display: flex;
    align-items: center;
}
.prueba {
    height: 100px;
    width: 100%;
    background: red;
}
</style>