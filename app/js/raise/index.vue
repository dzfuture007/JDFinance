<template lang="html">
    <div>
        <Heador/>
        <Slider/>
        <Daily/>
        <In/>
        <Fuli/>
        <Footor cname="mfooter"/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Navbar from "../public/navbar.vue"
import Footor from "../public/footer.vue"
import Slider from "./rslider.vue"
import Daily from "./daily.vue"
import In from "./in.vue"
import Fuli from "./fuli.vue"
export default {
    components: {
        Heador,
        Slider,
        Daily,
        In,
        Fuli,
        Footor,
        Navbar,
    },
}
</script>

<style lang="scss">
    .mfooter {
        margin-top: 0 !important;
        ul {
            li:first-child {
                display: none;
            }
        }
    }
</style>
