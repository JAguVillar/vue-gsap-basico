<template>
    <div class="main">
        <div class="container">
            <span class="palabra uno">Hola</span>
            <div style="display: inline" class="palabra tres">
                Agoto
                <div
                    class="linea"
                    style="width: 100%; height: 20px; background: pink"
                ></div>
            </div>
        </div>
    </div>
</template>

<script>
import { gsap } from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);
export default {
    name: "HelloWorld",
    data() {
        return {
            text: "Hello World",
        };
    },
    mounted() {
        let tl = gsap.timeline();
        const words = document.querySelectorAll(".container .palabra");

        words.forEach((word) => {
            tl.from(word, {
                opacity: 0,
                y: -20,
                duration: 0.5,
                // delay: index * 0.2, // Add a small delay to stagger the animations
                ease: "power2.out",
            });
        });
        tl.from(".linea", {
            opacity: 0,
            x: 100,
            ease: "power2.out",
            duration: 0.2,
        });
        gsap.to(".container", {
            scrollTrigger: {
                trigger: ".container",
                start: "top top",
                end: "bottom bottom",
                markers: true,
            },
            scale: 0.2,
            position: "fixed",
            top: 0,
            left: 0,
            width: "auto",

            duration: 0.5,
        });
    },
    methods: {},
};
</script>

<style scoped>
.main {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100vw;
    height: 100vh;
}
.container {
    display: flex;
    width: fit-content;
    height: 10px;
}
</style>
