<template>
<view class="centen">
	 <view>{{msg}}</view>
	 <view>{{money}}</view>
	 <view>{{isRech}}</view>
	 <view>{{parqe.name}}</view>
	 <view>{{parqe.skill}}</view>
	<!--  在标签上通过属性的方式来使用数据 -->
	 <view :data-color="color">color</view>
<view>====================================</view>
	 <view v-for="(item,index) in list"
	 :key="(item.id)"
	 >
	 {{item.id}}--{{item.text}}--{{index}}
	 </view>
<view>--------------------</view>
<view>{{cnMoney}}</view>
<view>{{filter}}</view>
</view>
</template>

<script>
	export default {
		//data定义数据
	    data(){
			return{
				//存放数据
				msg:"黑马程序员",
				//数字
				money:10000,
				//bool类型
			    isRech:false,
				//类型
				parqe:{
					name:"小明",
					skill:"72变",
				},
				color:"aqua",
				list:[
	        	{
		       	id:0,
	   	       	text:'小明'
	          	},
		     	{
		      	id:1,
		     	text:'小白'
	        	},
			   {
		    	id:2,
		    	text:'小红'
	        	},
	             ]
             	}
	    	},
		//2.计算属性
		computed:{
		cnMoney(){
		  return "$" +this.money	
	    	},
			//过滤数组
			filterList(){
				//只要id>0都不要显示
				return this.list.filter(v=>v.id<=0);
			}
		  }
		}
	 

</script>

<style>
	
</style>
