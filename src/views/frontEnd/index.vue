<!-- 前端导航 -->
<template>
  <div>
      <websiteList :websiteOptions = "frontOptions"></websiteList>
  </div>
</template>

<script>
import websiteList from '../../components/websiteList'
import { frontEndList } from '../../js/websiteList'
export default {
    data () {
        return {
            frontOptions: {
                title: '前端导航',
                dataList: frontEndList
            }
        }
    },
    components: { websiteList },
    mounted() {},

    methods: {}
}

</script>
<style lang='less' scoped>
</style>