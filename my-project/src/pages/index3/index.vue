<template>
	<view class="content">
     <!--2使用数据{{ msg }}-->>
	 <view>{{msg}}</view>
	 <view>{{ person.name}}</view>
	 <view>{{ person.skill}}</view>
	 <!--在标签上通过属性的方式使用数据-->
	 <view  :data-color="color">color</view>
	 <view>===================</view>
	 <view>
          <!-- 通过view标签显示-->
        <view
		 v-for="(item) in list"
		 :key="item.id"
		 >
      {{ item.id }} --{{ item.text}}
		</view>
    
	 </view>
	</view>
</template>

<script>
	export default {
	 //1 data定义数据
	 data(){
      return{
      //存放数据
	  msg:"优眠时光",
	  money:10000,
	  isRish:false,
	  person:{
          name:"白鹿",
		  skill:"猫"

	  },
	  color:"aqua",
	  //定义一个数组
	  list:[
        {         
        id:0,
		text:"管理员"

		},

		{
        id:1,
		text:"员工"
		},
		{
        id:2,
		text:"普通用户"
		}
      
	  ]
		
	  }

	 }

	}

</script>

<style lang="scss">

</style>
