<template>
  <div id="app">
    <button @click="open">打开弹框</button>
    <maucash-model
      v-model="model"
      title="标题"
    >内容体</maucash-model>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import maucashModel from './packages/maucash-model/MaucashModel.vue';

@Component({
  components: {
    maucashModel,
  },
})
export default class App extends Vue {
  private model: boolean = false;

  private open(): void {
    this.model = true;
  }
}
</script>

<style lang="scss">
</style>
