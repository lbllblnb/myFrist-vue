<template>
  <div id="app">
    <router-view></router-view>
    <tab-bar>
      <tabbar-item path="/home">
        <img slot="item-icon" src="./assets/img/tabbar/地址.png" />
        <div slot="item-text">首页</div>
      </tabbar-item>
      <tabbar-item path="/category">
        <img slot="item-icon" src="./assets/img/tabbar/书签 (2).png" />
        <div slot="item-text">分类</div>
      </tabbar-item>
      <tabbar-item path="/cart">
        <img slot="item-icon" src="./assets/img/tabbar/详细地址.png" />
        <div slot="item-text">购物</div>
      </tabbar-item>
      <tabbar-item path="/proflie">
        <img slot="item-icon" src="./assets/img/tabbar/房子.png" />
        <div slot="item-text">我的</div>
      </tabbar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from "./components/tabbar/Tabbar.vue";
import TabbarItem from "./components/tabbar/tabbarItem.vue";
export default {
  components: { TabBar, TabbarItem },
  name: "App",
};
</script>

<style>
@import "./assets/css/base.css";
</style>

