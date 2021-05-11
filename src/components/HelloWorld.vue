<template>
  <div class="hello">
    <h1>{{ state.testMsg }}</h1>
    <button @click="test"></button>
    <div @click="$router.push('/about')">test About</div>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive } from "vue"

export default defineComponent({
  name: "HelloWorld",
  props: {
    msg: String,
  },
  setup(props) {
    const state = reactive({
      testMsg: props.msg + "tesresrser",
    })
    const heheheh: string = "고정 값입니다."
    const test = (): void => {
      console.log("inini")
      state.testMsg = heheheh
      console.log(state.testMsg)
    }
    return {
      state,
      test,
    }
  },
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
