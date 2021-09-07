<template>
  <div class="tabbar-item">
    <div @click="itembtn"><slot name="item-icon"></slot></div>
    <div :style="activestyle"><slot name="item-text"></slot></div>
  </div>
</template>
<script>
export default {
  name: "tabbarItem",
  props: {
    path: String,
    activecolor: {
      type: String,
      default: "red",
    },
  },
  methods: {
    itembtn() {
      this.$router.replace(this.path);
    },
  },
  computed: {
    isactive() {
      return this.$route.path.indexOf(this.path) !== -1;
    },
    activestyle() {
      return this.isactive ? { color: this.activecolor } : {};
    },
  },
};
</script>
<style scoped>
.tabbar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tabbar-item img {
  width: 24px;
  height: 24px;
  vertical-align: middle;
  margin-bottom: 2px;
}
</style>
