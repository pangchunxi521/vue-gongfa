<template>
	<div id="show">
		<Head></Head>
		<List></List>
	</div>
</template>

<script>
import Head from './head.vue';
import List from './list.vue'
export default {
	name: '',
	data() {
		return {
			bbb: '222'
		};
	},
	components: {
		Head,
		List
	}
};
</script>

<style scoped>
	h1{
		font-size: 100px;
		text-align: center;
	}
	</style>