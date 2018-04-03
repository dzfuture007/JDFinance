<template>
    <div :class="$style.header">
        <span :class="$style.left">
            <!-- 这里不涉及登录注册的业务所以写成文本，真正开发的时候是router-link -->
            <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
        </span>
        <btn :class="$style.btnDownload">APP下载</btn>
    </div>
</template>

<script>
import btn from "../core/btn.vue"
export default {
    components: {
        btn,
    },
}
</script>

<style lang="scss" module>
    .header {
        color: #666;
        font-size: 32px;
        // 垂直居中
        height: 100px;
        line-height: 100px;
        // 吸顶效果
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        z-index: 100;
        // 背景图
        background: #fff url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat;
        background-size: auto 50%;
        .left {
            font-size: 28;
            height: 30;
            line-height: 30px;
            margin: 17px 0 0 18px;
        }
        .btnDownload {
            float: right;
            font-size: 24px;
            border-width: 0;
            height: 56px;
            line-height: 56px;
            min-width: 120px;
            padding: 0;
            border-radius: 4px;
            margin: 28px 24px 0 0;
        }
    }
</style>
