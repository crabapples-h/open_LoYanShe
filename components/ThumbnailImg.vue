<template>
  <img :src="thumbnailUrl" :title="title" alt="">
</template>
<script >
import Vue from 'vue'

export default {
  components: {},
  props: {
    url: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: ''
    },
    imageSize: {
      type: Number,
      default: 300
    }
  },
  data () {
    return {
    }
  },
  computed: {
    thumbnailUrl () {
      return `${Vue.prototype.BASE_IMG}${this.url}?x-oss-process=image/quality,q_80/resize,w_${this.imageSize}`
    }
  },
  watch: {
  },
  created () {
  },
  activated () {
  },
  mounted () {
  },
  methods: {

  }
}
</script>

<style scoped lang="less">

</style>
