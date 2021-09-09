<template>

  <n-card title="Card Slots Demo">
    <template #header-extra> #header-extra </template>
    <h5>{{ msg }}</h5>
    <template #footer> {{ name }} - {{ item }}</template>
    <template #action> <n-button @click="changeName('Tobby')">naive-ui</n-button> </template>
  </n-card>

</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { NCard, NButton } from 'naive-ui'

export default defineComponent({
  name: 'Card',
  components: {
    NCard,
    NButton
  },
  props: {
    msg: String,
    name: String,
  },
  data(){
    return {
      item: 'New Name' as string | number
    }
  },
  methods: {
    changeName(item: string | number){
      this.item = item 
    }
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
