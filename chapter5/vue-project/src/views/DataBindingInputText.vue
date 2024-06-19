<template>
    <div>
      <input type="text" v-model="valueModel">
    </div>
    <div>text에서 글자를 바꾸면 여기서 이렇게! {{valueModel}} 바뀝니다.</div>
</template>
<script>
export default {
  data () {
    return {
      valueModel: 'South Korea'
    }
  }
}
</script>
