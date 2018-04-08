<template lang="html">
    <div>
        <Heador/>
        <Slider/>
        <Weal/>
        <Service/>
        <Footor/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Navbar from "../public/navbar.vue"
import Footor from "../public/footer.vue"
import Slider from "./bslider.vue"
import Service from "./service.vue"
import Weal from "./weal.vue"

export default {
    components: {
        Heador,
        Slider,
        Weal,
        Footor,
        Service,
        Navbar,
    },
}
</script>

<style lang="scss">
</style>
