<template>

  <n-space vertical size="large">
    <n-layout>
      <n-layout-header>
        <Menu />
      </n-layout-header>
      <n-layout-content content-style="padding: 24px;">
        <router-view></router-view>
      </n-layout-content>
      <n-layout-footer>FOOTER</n-layout-footer>
    </n-layout>
  </n-space>

</template>

<script lang="ts">
import { defineComponent } from 'vue'
// UI
import { NLayout, NLayoutContent, NLayoutHeader, NLayoutFooter, NSpace  } from 'naive-ui'
// Components
import Menu from './components/Menu.vue'

export default defineComponent({
  name: 'App',
  components: {
    Menu,
    NLayout,
    NSpace,
    NLayoutContent,
    NLayoutHeader,
    NLayoutFooter
  }
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 0px;
}

.n-layout-footer {
  background: #000;
  padding: 24px;
  color:#fff;
}

.n-layout-sider {
  background: rgba(128, 128, 128, 0.3);
}

.n-layout-content {
  background: rgba(255, 255, 255, 0.4);
}
</style>
