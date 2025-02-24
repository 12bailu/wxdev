<template>
	<view class="content">
      <!--使用数据{{ msg }}-->
	  <view>{{msg}}</view>
	  <view>{{ money }}</view>
	  <view>{{isRish}}</view>
	  <view>{{person.name}}</view>
	  <view>{{person.skill}}</view>

	  <!--在标签上 通过属性的方式来使用数据-->
	  <view :data-color="color">color</view>

	  <view>========================</view>
	  <view>
		<!--list 通过view标签来显示-->
		<view
		v-for="(item,index) in list"
		:key="item.id"
		 >
        {{item.id}} --{{item.text}}--{{ index }}
		</view>
	  </view>
	  <view>------------------------</view>
	  <view>
		  <view v-if="true">显示</view>
		  <view v-show="false">隐藏</view>
	  </view>
	  <view>￥{{ money }}</view>
	  <view>￥{{cnMoney}}</view>
	</view>
</template>

<script>
	export default {
  //data定义数据
   data(){
	  return{
		//存放数据
		msg:"优眠时光",
		money:10000,
		isRish:false,
		//对象
		person:{
			name:"管理员",
			skill:"最高权限"

		},
		color:"aqua",
		//数组
		list:[
			{
				id:0,
				text:"用户0"
			},
			{
				id:1,
				text:"用户1"
			},
			{
				id:2,
				text:"用户2"
			},
			
			
		]
	  }
	
	},
	//2计算功能
	computed:{

		cnMoney(){
            //营业额
			return "￥"+this.money;

		}
	}

   }
//颜色

</script>

<style lang="scss">
   


</style>
