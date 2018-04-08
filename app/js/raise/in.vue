<template>
    <Panel title="In货推荐" :class="$style.panel">
        <section :class="$style.content">
            <div :class="$style.item" v-for="item in items" :key="item.catory">
                <img :src="item.catory" alt="">
                <section :class="$style.list">
                    <div :class="$style.product" v-for="product in item.products" :key="product.title">
                        <img :src="product.img" alt="">
                        <p :class="$style.title">{{ product.title }}}</p>
                        <p :class="$style.price"><em>{{ product.price }}</em>起</p>
                        <article>
                            <div :class="$style.wrapper">
                                <div :class="$style.inner" :style="{width:product.percent+'%'}"/>
                            </div>
                            <p>{{ product.percent }}%</p>
                        </article>
                        <label v-if="product.great">{{ product.great }}</label>
                    </div>
                </section>
            </div>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
    data() {
        return {
            items: [{
                catory: "//img12.360buyimg.com/jrpmobile/jfs/t3406/210/2247820735/50952/86016eea/5846d8e7N20446dbd.png?width=750&height=200",
                products: [{
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 460,
                    great: "精选",
                }, {
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 40,
                }, {
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 50,
                }, {
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 60,
                }],
            }, {
                catory: "//img12.360buyimg.com/jrpmobile/jfs/t3739/82/2244582797/54399/746c7d79/5846a953N66b67d05.png?width=750&height=200",
                products: [{
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 31,
                }, {
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 41,
                }, {
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 51,
                }, {
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 61,
                }],
            }, {
                catory: "//img12.360buyimg.com/jrpmobile/jfs/t3214/113/4408032436/61548/ce316eef/5846d310Ne93f00c9.png?width=750&height=200",
                products: [{
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 71,
                }, {
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 81,
                }, {
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 91,
                }, {
                    img: "//img12.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.png",
                    title: "双响炮蓝牙音箱",
                    price: "26.99",
                    percent: 99,
                }],
            }],
        }
    },
}
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel;
        .content {
            @include list;
            .item {
                margin-bottom: 40px;
                >img {
                    display: block;
                    width: 100%;
                    height: 170px;
                }
                .list {
                    @include list(row);
                    .product {
                        width: 50%;
                        height: 396px;
                        box-sizing: border-box;
                        background-color: rgba(0, 0, 0, .02);
                        text-align: center;
                        position: relative;
                        img {
                            margin: 44px auto 20px;
                            width: 180px;
                            height: 180px;
                        }
                        .title {
                            font-family: serif;
                            font-size: 28px;
                            font-weight: 700;
                            color: #444;
                        }
                        .price {
                            font-family: serif;
                            font-size: 20px;
                            color: #999;
                            line-height: 48px;
                            em {
                                color: #FF3232;
                                font-size: 36px;
                                margin-right: 8px;
                                &::before {
                                    content: "￥";
                                    color: #FF3232;
                                    font-size: 28px;
                                }
                            }
                        }
                        article {
                            @include list(row);
                            align-items: center;
                            justify-content: space-around;
                            padding: 0 20px;
                            line-height: 30px;
                            margin-top: 16px;
                            .wrapper {
                                width: 144px;
                                height: 10px;
                                background-color: #F6E6E6;
                                border-radius: 22px;
                                .inner {
                                    width: 40px;
                                    max-width: 100%;
                                    height: 10px;
                                    background-image: linear-gradient(270deg, #F55 1%, #FF9C31 100%);
                                    border-radius: 22px;
                                }
                            }
                            p {
                                font-size: 24px;
                                color: #999;
                            }
                        }
                    }
                    label {
                        position: absolute;
                        left: 0;
                        top: 0;
                        font-family: serif;
                        font-size: 20px;
                        color: red;
                        text-align: center;
                        padding: 4px 8px;
                        background-image: linear-gradient(-35deg, #C1C1C1 0, #ACACAC 100%);
                    }
                }
            }
        }
    }
</style>
