<script>
import BaseFooter from "./components/BaseFooter";

export default {
  components: {
    BaseFooter
  }
};
</script>

<template>
  <div id="app">
    <router-view />
    <base-footer />
  </div>
</template>

<style lang="scss">
@import "./styles/index";

#app {
  min-height: calc(100% - 40px);
}
</style>
