<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back">&#xe624;</div>
        </div>
        <div class="header-input">
            <span class="iconfont search">&#xe632;</span>
            输入城市/景点/游玩主题
        </div>
        <div class="header-right">
            {{this.city}}
            <span class="iconfont arrow">&#xe6aa;</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    .header
        display flex
        line-height .86rem
        background $bgColor
        color #ffffff
        .header-left
            width .64rem
            float left
            .back
                margin-left .2rem
        .header-input
            flex 1
            height .64rem
            line-height .64rem
            margin-top .12rem
            margin-left .2rem
            background #ffffff
            border-radius .1rem
            color #cccccc
            .search
                margin-left .1rem
        .header-right
            width 1.24rem
            float right
            text-align center
            .arrow
                margin-left -.1rem
                font-size .25rem
</style>
