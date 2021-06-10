<template>
	<view class="content">
	<!-- 4 使用组件 -->
<!--<imgBorder></imgBorder> -->
    <view>子组件传递过来的数据{{src}}</view>
	<img-border @srcChange="handlesrcChange" :src="src1"></img-border>
	<img-border @srcChange="handlesrcChange" :src="src2"></img-border>
	</view>
	
</template>

<script>
//2引入自定义组件
import imgBorder from "@/components/img-border";
	export default {
		data(){
           return{
          src:"src",
		  src1:"https://gimg2.baidu.com/image_search/src=http%3A%2F%2Ffjmingfeng.com%2Fimg%2F5%2F3088218851%2F62%2F1dce18c2a9fba7e1d1a0076116803403%2F9209081442%2F4712615793.jpg&refer=http%3A%2F%2Ffjmingfeng.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1623072095&t=3f6d7b3a770447cd4eaeecbcaf10e12f",
		  src2:"https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.doutula.com%2Fproduction%2Fuploads%2Fimage%2F2017%2F10%2F26%2F20171026030310_ZtYIPr.gif&refer=http%3A%2F%2Fimg.doutula.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1623237034&t=b522ae49e5ddef3d185e59aeaf669856"
		}
		},
	    //3注册组件
		components:{
			imgBorder
		},
		methods:{
		handlesrcChange(e){
			/* 父组件的自定义事件被触发了 */
			this.src=e
		},
	
	  },
	  //onload 页面加载完毕就会触发 生命周期
	  	onLoad(){
			console.log(this.baseurl);	
            console.log(getApp().globalData.base);
		},
		
		
	}
</script>

<style>

</style>
