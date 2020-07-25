<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back">&#xe624;</div>
        </div>
        <div class="header-input">
            <span class="iconfont search">&#xe632;</span>
            输入城市/景点/游玩主题
        </div>
        <router-link to="/city">
            <div class="header-right">
                {{this.city}}
                <span class="iconfont arrow">&#xe6aa;</span>
            </div>
        </router-link>
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
        display: flex
        line-height: $headerHeight
        background: $bgColor
        color: #ffffff
        .header-left
            width: .64rem
            float: left
            .back
                margin-left: .2rem
        .header-input
            flex: 1
            height: .61rem
            line-height: .61rem
            margin-top: .12rem
            margin-left: .2rem
            background: #ffffff
            border-radius: .1rem
            color: #cccccc
            .search
                margin-left: .1rem
        .header-right
            width: 1.24rem
            float: right
            text-align: center
            color: #ffffff
            .arrow
                margin-left: -.1rem
                font-size: .25rem
</style>
