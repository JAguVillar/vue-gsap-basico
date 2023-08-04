<template>
    <div class="main">
        <div class="left">
            <h1 class="titulo">
                <span class="palabra">Pouches</span>
                <span class="palabra">with</span>
                <span class="palabra">your</span>
                <span class="palabra">
                    <div class="pill"></div>
                    print
                </span>
            </h1>
            <div class="intro">
                Truly sustainable packaging solutions that will take your
                products to a whole new level. Get a high-end look for the same
                price as a blank pouch with a label.
            </div>
        </div>
        <div class="right">
            <img src="/images/lprint-2.0.png" alt="" srcset="" />
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
        return {};
    },
    // mounted() {
    //     // let tl = gsap.timeline();
    //     let tl = gsap.timeline();
    //     const words = document.querySelectorAll(".titulo .palabra");

    //     words.forEach((word) => {
    //         tl.from(word, {
    //             opacity: 0,
    //             y: 20,

    //             stagger: 1, // stagger start times
    //             ease: "power2.out",
    //         }).add("end");
    //     });
    //     tl.from(".intro", { opacity: 0 }, "end");
    //     tl.from(".pill", { width: 0 }, "end");
    // },
    methods: {},
};
</script>

<style scoped>
.main {
    position: relative;
    display: flex;
    flex-direction: row;
    width: 100vw;
    height: 100vh;
    margin: 0 auto;
}
.left {
    position: relative;
    width: 50%;
    background: #fff;
    display: flex;
    justify-content: center;

    flex-direction: column;
}
.titulo {
    font-weight: 400;
    font-size: 80px;
    padding: 0px 20px;
    z-index: 5;
    position: relative;
}
.right {
    width: 50%;
    background: #ffd124;
    display: flex;
    justify-content: center;
    align-items: center;
    padding-right: 20px;
}

img {
    max-width: 60%;
    max-height: 65%;
}
.palabra {
    display: inline-block;
    margin: 0px 10px;
    position: relative;
}
.pill {
    overflow: hidden;
    background: #ffd124;
    border-radius: 70px;
    height: 105px;
    position: absolute;
    width: 100%;
    z-index: 0;
    top: 16px;
    z-index: -1;
}

.intro {
    padding-left: 40px;
    margin-top: 24px;
    font-size: 16px;
    line-height: 1.5;
    letter-spacing: 0.02em;
    color: #000000;
    opacity: 0.8;
    max-width: 355px;
}
</style>
