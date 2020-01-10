<template>
  <div class="home">
    <Select></Select>

    <van-datetime-picker
        v-model="currentDate"
        type="datetime"
        :min-date="minDate"
        :max-date="maxDate"
    />


    <van-circle
        v-model="currentRate"
        :rate="30"
        :speed="100"
        :text="text"
    />
   
    <Coupon></Coupon>
    <!-- <van-action-sheet v-model="show" :actions="actions" @select="onSelect(item)" /> -->
  </div>
</template>

<script>
// import Select from './Select'
// import Coupon from './Coupon'
export default {
    // components:{
    //   Select,
    //   Coupon
    // },
    data() {
    return {
      minDate: new Date(2020, 0, 1),
      maxDate: new Date(2025, 10, 1),
      currentDate: new Date(),
      
       currentRate: 0
    //   show: false,
    //   actions: [
    //     { name: '选项' },
    //     { name: '选项' },
    //     { name: '选项', subname: '描述信息' }
    //   ]
    };
    
  },

    computed: {
        text() {
        return this.currentRate.toFixed(0) + '%'
        }
    }

    // methods: {
    //     onSelect(item) {
    //         console.log(item)
    //     // 默认情况下，点击选项时不会自动关闭菜单
    //     // 可以通过 close-on-click-action 属性开启自动关闭
    //     this.show = false;
    //     Toast(item.name)
    //     }
    // }
 }

</script>