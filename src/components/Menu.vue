<template>

    <n-menu v-model:value="activeKey" mode="horizontal" :options="menuOptions" class='menu' />

</template>

<script lang="ts">
import { defineComponent, h, ref } from 'vue'
import { NMenu, NIcon } from 'naive-ui'
import { HomeOutline, PersonOutline } from '@vicons/ionicons5'

function renderIcon (icon:any) {
  return () => h(NIcon, null, { default: () => h(icon) })
}

const menuOptions = [
  {
    label: () =>
      h(
        'a',
        {
          href: '/',
          //target: '_blank',
          rel: 'noopenner noreferrer'
        },
        'Home'
      ),
    key: 'hear-the-wind-sing',
    icon: renderIcon(HomeOutline)
  },
  {
    label: () =>
      h(
        'a',
        {
          href: '/employees',
          //target: '_blank',
          rel: 'noopenner noreferrer'
        },
        'Employees List'
      ),
    key: 'hear-the-wind-sing',
    icon: renderIcon(PersonOutline)
  },
]


export default defineComponent({
  name: 'Menu',
  components: {
    NMenu,
  },
  setup () {
    return {
      activeKey: ref(null),
      menuOptions
    }
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .menu {
    background-color: #ccc;
    width: 100%;
  }
</style>
