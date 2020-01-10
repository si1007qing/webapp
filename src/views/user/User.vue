<template lang="html">
<div>
  <h1 @touchstart='click'>个人中心</h1>
  <TabBar></TabBar>
</div>
</template>

<script>
const TabBar = ()=>import('@/components/TabBar.vue')
export default {
  components: {
    TabBar
  },
  methods:{
    click(){
      // console.log(idx)
      console.log(1)
      this.$router.replace('/homework')
    }
  }
}
 
</script>

<style lang="css" scoped>
</style>
