<template>
  <div>
    <nav-bar class="nav-bar">
      <div slot="center">购物车({{cartLength}})</div>
    </nav-bar>
  </div>
</template>

<script>
import NavBar from "components/common/navbar/NavBar";
export default {
  name: "Cart",
  components: {
    NavBar,
  },
  computed: {
    cartLength() {
      return this.$store.state.cartList.length;
    },
  },
};
</script>

<style scoped>
.nav-bar {
  color: #fff;
  background-color: var(--color-tint);
}
</style>
