<template>
    <div class="main"></div>
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
        gsap.timeline({
            scrollTrigger: {
                trigger: ".orangeWrapper",
                scrub: true,
                pin: true,

                start: "50% 50%",
                end: "+=200%",
            },
        })

            .from(".orange", {
                scale: 0.5,
                ease: "none",
            })

            .from(
                ".line-2",
                {
                    scaleX: 0,
                    ease: "none",
                    transformOrigin: "left top",
                },
                0
            );
    },
    methods: {},
};
</script>
<style scoped>
.main {
    height: 100vh;
}
</style>