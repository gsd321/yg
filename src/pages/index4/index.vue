<template>
 <view class="content">
    <view data-index="11" @click="handleClick(1,$event)">点我试试1</view>
	<view data-index="22" @click="handleClick(2,$event)">点我试试2</view>
 </view>
</template>

<script>
	export default {
		//2在methods里面来定义事件的回调
	      methods:{
			  handleClick(index,event){
				  console.log(index);
				  console.log(event);
				  console.log(event.currentTarget.dataset.index);
			  }
		  }
	}
</script>

<style>

</style>
