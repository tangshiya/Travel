<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{city}}
        <span class="iconfont city-icon">&#xe6aa;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  computed: {
    city () {
      return this.$store.state.city
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.header {
  height: 0.86rem;
  line-height: 0.86rem;
  background-color: $bgColor;
  color: #fff;
  display: flex;

  .header-left {
    width: 0.64rem;
    float: left;

    .back-icon {
      font-size: 0.4rem;
      display: block;
      text-align: center;
    }
  }

  .header-input {
    flex: 1;
    margin-top: 0.12rem;
    // margin-left: 0.2rem;
    height: 0.62rem;
    line-height: 0.62rem;
    border-radius: 0.1rem;
    background-color: #fff;
    color: #ccc;
    padding-left: 0.2rem;
  }

  .header-right {
    min-width: 1.04rem;
    padding: 0 0.1rem;
    float: right;
    text-align: center;
    color: #fff;

    .city-icon {
      margin-left: -0.08rem;
    }
  }
}
</style>
