<template>
	<div class="list ">
		<ul class="lis clearfloat">
			<li v-for="item in lists" :key="item.id" class="one">
				<Icon type="ios-car" size="80" />
				<h3>{{ item.title }}</h3>
				<span>{{ item.content }}</span>
				<p class="pa">
					<a :href="href">
						<router-link to="/Serve"><i>{{ msg }}</i></router-link>
					</a>
				</p>
			</li>
		</ul>

		<div class="linea">
			<Divider dashed><p>最新动态</p></Divider>
		</div>

		<ul class="lis clearfloat" id="list2">
			<li v-for="son in listsa" :key="son.id" class="one">
				<div><img :src="son.src" alt="" /></div>
				<h3>{{ son.title }}</h3>
				<span>
					<i>{{ son.content }}</i>
				</span>
				<p class="alt">
					<a :href="href" @mouseenter="chang()" v-show="com">
						<span><Icon type="ios-search" size="30" :color="color" /></span>
					</a>
					<a :href="href" @mouseleave="change()" v-show="!com">
						<span><Icon type="ios-search" size="30" :color="color1" /></span>
					</a>
					<a :href="href" @mouseenter="cli()" v-show="xian">
						<span><Icon type="ios-link" size="30" :color="color" /></span>
					</a>
					<a :href="href" @mouseleave="clie()" v-show="!xian">
						<span><Icon type="ios-link" size="30" color="#dd5a01" /></span>
					</a>
				</p>
			</li>
		</ul>

		<div class="linea lineb">
			<Divider dashed>
				<p>
					租车客车到共发
					<br />
					的5大理由
				</p>
			</Divider>
		</div>
		<Txt></Txt>
		
		<!-- <div class="liyou">
			 <Carousel
				v-model="value3"
				:autoplay="setting.autoplay"
				:autoplay-speed="setting.autoplaySpeed"
				:dots="setting.dots"
				:radius-dot="setting.radiusDot"
				:trigger="setting.trigger"
				:arrow="setting.arrow">
				<CarouselItem>
					<div class="demo-carousel">
						<p>
							2012年9月成立，注册资金人民币500万元，北京市交通委运管局备案。多年大客车租赁经验，服务客户众多，行业良好口碑。
						</p>
					</div>
				</CarouselItem>
				<CarouselItem>
					<div class="demo-carousel">
						<p>
							驾驶员均为A本老师傅，驾驶技术优良，素质高，服务好，安全意识强。熟悉山西及周边各条道路交通路况。...
						</p>
					</div>
				</CarouselItem>
				<CarouselItem>
					<div class="demo-carousel">
						<p>
							全部车辆开通免费WIFI，四季舒适的冷暖空调，DVD音响系统、麦克风，移动充电宝，豪华舒适座椅、安全带。...
						</p>
					</div>
				</CarouselItem>
				<CarouselItem>
					<div class="demo-carousel">
						<p>
							车辆均为2年左右新车，日常专业服务站维修保养，确保车款良好。可为一年以上新班车客户或者长租客户订购0公里新车。...
						</p>
					</div>
				</CarouselItem>
				<CarouselItem>
					<div class="demo-carousel">
						<p>
							所有车辆安装GPS全球定位系统
						</p>
					</div>
				</CarouselItem>
			</Carousel>
		</div> -->
	</div>
</template>

<script>
import Txt from './textplay.vue'
export default {
	name: '',
	data() {
		return {
			msg: '阅读更多',
			com: false,
			xian: true,
			color: '#fff',
			color1: '#ff5a01',
			href: 'javascript:;',
			asrc: 'https://www.haoyi23.com/static/assets/img/carinfo/15.png',
			lists: [
				{
					id: 0,
					title: '长期包租用车',
					content: ' 为常驻运城或临近省市的企业、办事机构提供各类用车，可长期包租...'
				},
				{
					id: 1,
					title: '旅游用车',
					content: ' 为常驻运城或临近省市的企业、办事机构提供各类用车，可长期包租...'
				},
				{
					id: 2,
					title: '市民用车',
					content: '我公司备有中低档轿车、面包车等车型，可供本市市民租用...'
				},
				{
					id: 3,
					title: '婚庆用车',
					content: ' 为个人或婚庆公司提供高档婚庆车和车队服务...'
				}
			],
			listsa: [
				{
					id: 0,
					src: 'https://www.haoyi23.com/static/assets/img/carinfo/15.png',
					title: '山西运城共发车队',
					content: '用车不用东奔西走, 共发车队应有尽有.☎️:15235903198～～13191198482...'
				},
				{
					id: 1,
					src: 'https://www.haoyi23.com/static/assets/img/carinfo/19.png',
					title: '山西运城共发车队',
					content: '用车不用东奔西走, 共发车队应有尽有.☎️:15235903198～～13191198482...'
				},
				{
					id: 2,
					src: 'https://www.haoyi23.com/static/assets/img/carinfo/45.png',
					title: '山西运城共发车队',
					content: '用车不用东奔西走, 共发车队应有尽有.☎️:15235903198～～13191198482...'
				},
				{
					id: 3,
					src: 'https://www.haoyi23.com/static/assets/img/carinfo/53.png',
					title: '山西运城共发车队',
					content: '用车不用东奔西走, 共发车队应有尽有.☎️:15235903198～～13191198482...'
				}
			]
			
		};
	},
	methods: {
		// 		chang:function(){
		// 				for(var i=0;i<this.listsa.length;i++){
		// 					console.log(this.color)
		// 					this.color = "#fff"?"#ff5a01":"#fff"
		// 		    }
		// 	    }
		//          chang:function(index){
		// 			 this. i = index
		// 		 }
		chang: function() {
			this.com = !this.com;
			console.log('循环');
		},
		change: function() {
			this.com = true;
		},
		cli: function() {
			this.xian = !this.xian;
		},
		clie: function() {
			this.xian = false;
		}
	},
	created: function() {
		console.log('执行到这里');
		setInterval(this.chang, 1000);
		setInterval(this.cli, 1000);
	},
	components:{
		Txt
	}
};
</script>

<style scoped="">
.clearfloat:after {
	content: '.';
	display: block;
	visibility: hidden;
	height: 0;
	clear: both
}
.list {
	width: 100%;
	/* height: 1308px; */
	margin: 0 auto;
	background: #ffffee;
}
.lis {
	width: 1150px;
	/* height: 260px; */
	margin: 0 auto;
	padding-top: 40px;
}
.one {
	list-style: none;
	float: left;
	width: 246px;
	height: 240px;
	text-align: center;
	background: #f8f8f8;
	/* background: #f40; */
	border-radius: 2px;
	margin: 0 20px 0;
	padding: 15px 15px 20px 15px;
	border-bottom: 2px solid #9d426b;
}
.one:hover {
	box-shadow: inset 0px 0px 35px #dcdee2;
}
.one p {
	margin-top: 13px;
	font-family: 'Droid Sans', sans-serif;
	font-size: 14px;
	color: #5d5d5d;
	font-weight: bold;
	text-transform: uppercase;
	text-shadow: 0 1px 0 rgba(255, 255, 255, 0.7);
	/* background: -webkit-linear-gradient(left, red , blue); */
}
.one span {
	padding-bottom: 7px;
	line-height: 24px;
}
.one .pa a {
	display: inline-block;
	padding: 5px 22px;
	background: #9d426b;
	color: #fff;
	text-shadow: none;
}
.linea {
	width: 1150px;
	margin: 50px auto 0;
}
.lineb {
	margin-top: 50px;
}
.linea p {
	width: 220px;
	margin: 0 auto;
	background: #fff;
	font-family: 'Lobster', cursive;
	font-size: 24px;
	color: #5d5d5d;
	font-weight: bold;
	border-radius: 10px;
}
#list2 .one {
	height: 350px;
}
#list2 .one .alt a {
	display: inline-block;
	width: 40px;
	height: 40px;
	margin: 5px;
	padding-top: 5px;
	border-radius: 50%;
	text-align: center;
	background: #9d426b;
	color: #fff;
	text-shadow: none;
}
#list2 .one .alt a:hover {
	background: #5d5d5d; /* ff5a01 */
}

</style>
