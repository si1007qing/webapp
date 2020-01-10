<template lang="html">
<div>
  <h1>详情页</h1>
  <h1 v-text='$route.params.id'></h1>
  <!--  <van-index-anchor index="1">标题1</van-index-anchor>
     <van-cell title="文本" />
     <van-cell title="文本" />
     <van-cell title="文本" />
   
     <van-index-anchor index="2">标题2</van-index-anchor>
     <van-cell title="文本" />
     <van-cell title="文本" />
     <van-cell title="文本" /> -->
	 <van-nav-bar
	   title="标题"
	   left-text="返回"
	   right-text="按钮"
	   left-arrow
	   @click-left="onClickLeft"
	   @click-right="onClickRight"
	 />
</div>
</template>

<script>

export default {
  mounted() {
    console.log(this.$route)
   
  },
   // data() {
   //    return {
   //      indexList: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
   //    }
   //  },
	methods: {
	    onClickLeft() {
	      Toast('返回');
	    },
	    onClickRight() {
	      Toast('按钮');
	    }
	  }
  
}
</script>

<style lang="css" scoped>
</style>
