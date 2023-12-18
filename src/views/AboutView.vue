<script>
import { Snackbar } from '@varlet/ui'
export default {
  // reactive state
  data() {
    return {
      count1: 0,
      count2: 99, 
      count3: 66
    }
  },
  
  // functions that mutate state and trigger updates
  methods: {
    increment() {
      this.count1++; this.count2--
    },
    decrease() {
      this.count3--
    }
  },
  
  // lifecycle hooks
  mounted() {
    console.log(`The initial count is ${this.count1}.`)
    console.log(`The initial count is ${this.count2}.`)
    console.log(`The initial count is ${this.count3}.`)
  }
}
</script>

<template>
  <div class="about">
    <button @click="decrease">这个点一下会-1:{{ count3 }}</button>
    <br>
    <var-space :size="[10, 10]">
    <var-button type="success"  @click="increment">
      王老师戳了我{{ count1 }}下，剩余{{ count2 }}下
    </var-button>
  </var-space>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>

