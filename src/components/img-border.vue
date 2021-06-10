<template>
<!-- 1定义 -->
	<image @click="handleClick" class="img-border" :src="src"></image>

</template>

<script>
	export default {
		//声明一下接收的父组件传递过来的属性
	     props:{
			 src:String
		 },
		 methods:{
			 handleClick(e){
				 /*  console.log(e); */
				/*  子向父传递数据 通过触发事件  */
				 /* this.$emit("自定义的事件名称","要传递的参数") */
				 this.$emit("srcChange",this.src)
			 }
		 }
	}
</script>

<style>
.img-border{
    border-radius: 50%;
}
</style>