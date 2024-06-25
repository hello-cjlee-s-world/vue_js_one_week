<template>
  <div>
    <button type="button" @click="increaseCounter">Add 1</button>
    <button type="button" @click="setCount(7)">Set 7</button>
    <button type="button" @click="one">Set 1</button>
    <button type="button" @click="two">Set 2</button>
    <p>The counter is {{ counter }}</p>
  </div>
</template>
<script>
export default {
  data () {
    return {
      counter: 0
    }
  },
  methods: {
    increaseCounter () {
      this.counter = this.counter + 1
      console.log(this.counter)
    },
    setCount (counter) {
      this.counter = counter
    },
    one () {
      this.counter = 1
      alert(1)
    },
    two () {
      this.counter = 2
      alert(2)
    }
  }
}
</script>
