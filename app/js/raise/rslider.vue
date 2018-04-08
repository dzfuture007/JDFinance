<template>
    <Panel title="极速借贷" :class="$style.panel">
        <section :class="$style.content">
            <swiper :options="options">
                <swiper-slide v-for="item in items" :key="item.text">{{ item.text }} <em>></em></swiper-slide>
            </swiper>
        </section>
    </Panel>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper"
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
        swiper,
        swiperSlide,
    },
    data() {
        return {
            items: [{
                text: "百万白条券免费送，速来领取！",
            }, {
                text: "签到领流量，1元500M！",
            }],
            options: {
                autoplay: true,
                loop: true,
                direction: "vertical",
            },
        }
    },
}
</script>

<style lang="scss">
    .swiper-container-vertical {
        height: 72px;
        .swiper-slide {
            font-family: serif;
            font-size: 28px;
            color: #333;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
            em {
                color: #ddd;
                margin-right: 20px;
                float: right;
            }
        }
    }
</style>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel;
        margin-top: 120px !important;
        >h4 {
            display: none;
        }
        .content {
            height: 72px;
            line-height: 72px;
            padding-left: 178px;
            overflow: hidden;
            background: url(//m.jr.jd.com/spe/qyy/main/images/scroll_title_img.png) left top no-repeat;
        }
    }
</style>

