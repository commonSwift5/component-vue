<template>
	<div class="my_div">
		<img :src="imgSrc" alt="" />
		<p @click="changcolor" :style="{ backgroundColor: color }">{{ dogName }}</p>
	</div>
</template>

<script>
export default {
	props: {
		dogName: {
			type: String,
			default: '小米'
		},
		imgSrc: {
			type: String,
			default: 'https://scpic.chinaz.net/files/pic/pic9/202003/zzpic23514.jpg'
		}
	},
	data() {
		return {
			color: `rgb(${Math.random() * 256},${Math.random() * 256},${Math.random() * 256}) `
		}
	},
	methods: {
		changcolor() {
			this.color = `rgb(${Math.random() * 256},${Math.random() * 256},${Math.random() * 256}) `
		}
	}
}
</script>

<style>
.my_div {
	width: 200px;
	border: 1px solid black;
	text-align: center;
	float: left;
}

.my_div img {
	width: 100%;
	height: 200px;
}
</style>
