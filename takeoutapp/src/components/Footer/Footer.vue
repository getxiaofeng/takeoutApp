<template>
    <div class="footer_guide">
        <span class="guide_item"  :class="{on: '/shop'===$route.path}" @click="goTo('/shop')">
            <span class="item_icon">
            <i class="iconfont iconfenzu4"></i>
            </span>
            <span>外卖</span>
        </span>
        <span class="guide_item" :class="{on: '/search'===$route.path}" @click="goTo('/search')">
            <span class="item_icon">
            <i class="iconfont iconfenzu"></i>
            </span>
            <span>搜索</span>
        </span>
        <span class="guide_item" :class="{on: '/order'===$route.path}" @click="goTo('/order')">
            <span class="item_icon">
            <i class="iconfont iconfenzu6"></i>
            </span>
            <span>订单</span>
        </span>
        <span class="guide_item" :class="{on: '/user'===$route.path}" @click="goTo('/user')">
            <span class="item_icon">
            <i class="iconfont iconfenzu1"></i>
            </span>
            <span>我的</span>
        </span>
    </div>
</template>

<script>
    export default{
        methods:{
            goTo (path) {
                this.$router.replace(path)
            }
        }
    }
</script>

<style lang="stylus" rel="styleshet/stylus">
    @import "../../common/stylus/mixins.styl"
    .footer_guide
        top-border-1px(#e4e4e4)
        position fixed
        z-index 100
        left 0
        right 0
        bottom 0
        background-color #fff
        width 100%
        height 50px
        display flex
        .guide_item
            display flex
            flex 1
            text-align center
            flex-direction column
            align-items center
            margin 5px
            color #999999
            &.on
                color #0022bb
            span
                font-size 12px
                margin-top 2px
                margin-bottom 2px
                .iconfont
                    font-size 22px
</style>