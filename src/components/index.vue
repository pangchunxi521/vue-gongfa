<template>
	<div id="index">
		<Head></Head>
		<div class="player">
			<!-- banner轮播 -->
			<div class="row">
				<Carousel v-model="value3" loop autoplay>
					<CarouselItem>
						<div class="demo-carousel posie">
							<img src="https://www.haoyi23.com/static/assets/img/slider/1.jpg" alt="" />
						</div>
						<p class="tela">
							<span>
								<i>{{ items[0].hua }}</i>
							</span>
						</p>
					</CarouselItem>

					<CarouselItem>
						<div class="demo-carousel posie">
							<img src="https://www.haoyi23.com/static/assets/img/slider/2.jpg" alt="" />
						</div>

						<p class="tela">
							<span>
								<i>{{ items[1].hua }}</i>
							</span>
						</p>
					</CarouselItem>
					<CarouselItem>
						<div class="demo-carousel posie">
							<img src="https://www.haoyi23.com/static/assets/img/slider/3.jpg" alt="" />
						</div>
						<p class="tela">
							<span>
								<i>{{ items[2].hua }}</i>
							</span>
						</p>
					</CarouselItem>

					<CarouselItem>
						<div class="demo-carousel posie">
							<img src="https://www.haoyi23.com/static/assets/img/slider/4.jpg" alt="" />
						</div>

						<p class="tela">
							<span>
								<i>{{ items[3].hua }}</i>
							</span>
						</p>
					</CarouselItem>
				</Carousel>
				<div class="breviary">
					<img src="https://www.haoyi23.com/static/assets/img/slider/1.jpg" alt="" />
					<img src="https://www.haoyi23.com/static/assets/img/slider/2.jpg" alt="" />
					<img src="https://www.haoyi23.com/static/assets/img/slider/3.jpg" alt="" />
					<img src="https://www.haoyi23.com/static/assets/img/slider/4.jpg" alt="" />
				</div>
			</div>
		</div>

		<div class="wel">
			<h2>
				欢迎来到
				<span class="violet">{{ welcome }}</span>
				,一个安全 便捷 惠民 的用车平台
			</h2>
			<p>{{ swel }}</p>
		</div>

		<List></List>
		
		<Foot></Foot>
	</div>
</template>

<script>
import '../assets/play.css'
import Head from './head.vue'
import List from './list.vue'
import Foot from './foot.vue'

export default {
	name: '',
	data() {
		return {
			value3: 0,
			welcome: '共发车队',
			swel: '公司以安全第一为原则,为您的出行保驾护航',
			items: [
				{
					path: '.././assets/1.jpg',
					hua: '用车不用东奔西走, 共发车队应有尽有.☎️:15235903198～～13191198482'
				},
				{
					path: '.././assets/2.jpg',
					hua: '全国范围内出租大巴、中巴、各类车型。☎️:15235903198～～13191198482'
				},
				{
					path: '.././assets/3.jpg',
					hua: '全国范围内出租大巴、中巴、各类车型。☎️:15235903198～～13191198482'
				},
				{
					path: '.././assets/4.jpg',
					hua: '共发车队,安全从我做起 , 尊重 您 我 他.'
				}
			]
		};
	},
	components: {
		Head,
		List,
		Foot
	},
	methods: {
		change: function() {}
	}
};
</script>

<style scoped>

.player {
	width: 100%;
	padding: 3px;
	background: url(https://www.haoyi23.com/static/assets/img/pattern.jpg) repeat left top;
	padding-top: 10px;
	box-shadow: 0 5px 15px 0 rgba(0,0,0,.05) inset, 0 -5px 15px 0 rgba(0,0,0,.05) inset;
}
.row {
	width: 953px;
	margin: 0 auto;
	border: 10px solid #fff;
}
.ivu-carousel {
	width: 953px;
	height: 330px;
	margin: 0 auto;
}
.ivu-carousel-dots li button {
	height: 0.4375rem;
}
.posie {
	position: relative;
}
.posie img {
	width: 100%;
	height: 330px;
}
.tela {
	position: absolute;
	background: rgba(0, 0, 0, 0.5);
	width: 100%;
	bottom: 30px;
	text-align: left;
	height: 50px;
	padding: 10px;
}
span {
	font-size: 20px;
	line-height: 30px;
	color: #eaeaea;
}
.breviary {
	width: 960px;
	margin: 5px 0 0 10px;
}
.breviary img {
	margin: 0;
	padding: 0;
	width: 230px;
	height: 80px;
}
.wel {
	width: 100%;
	height: 90px;
	padding-top: 30px;
	background: #ffffee;
	text-align: center;
}
.wel h2 {
	font-family: 'Lobster', cursive;
	font-size: 30px;
	color: #5d5d5d;
	font-weight: bold;
}
.violet {
	font-size: 30px;
	color: #9d426b;
}
.wel p {
	font-size: 18px;
	font-style: italic;
	line-height: 20px;
}
</style>
