<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 @click="onChildChanged(msg)">Essential Links</h2>
    <Cart/>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Watch } from 'vue-property-decorator'
import Cart from '@/components/Cart.vue'
@Component({
  components: {
    Cart
  }
})
export default class Helloworld extends Vue {
  msg: string = '123'
  @Watch('child')
  onChildChanged (val: string, oldVal: string) {
    this.msg = '89565'
    console.log(this.msg)
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
