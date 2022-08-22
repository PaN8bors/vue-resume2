<template>
	<div class="hello">
		<!-- <p align="center">
			<a href="./files/Parish-resume.pdf" download>DOWNLOAD</a>
		</p> -->
		<div class="parent">
			<div class="div1"><img src="@/assets/headshot.jpg" /></div>
			<div class="div2">
				<div class="name">Parish A. Neighbors</div>
				<div class="contact-info">pn8bors@gmail.com</div>
				<div class="contact-info">(816) 674-9001</div>
			</div>
			<div class="div3"><DivThree /></div>
			<div class="div4"><DivFour /></div>
		</div>
	</div>
</template>

<script>
import DivThree from "@/components/DivThree.vue";
import DivFour from "@/components/DivFour.vue";

export default {
	name: "HelloWorld",
	components: {
		DivThree,
		DivFour,
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
	width: 80%;
	margin-left: auto;
	margin-right: auto;
	padding: 30px 0px;
	box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 30px 0 rgba(0, 0, 0, 0.19);
}
.parent {
	display: grid;
	grid-template-columns: repeat(5, 1fr);
	grid-template-rows: repeat(4, 1fr);
	grid-column-gap: 20px;
	grid-row-gap: 20px;
}
.div1 {
	grid-area: 1 / 1 / 2 / 3;
	display: flex;
	flex-direction: row-reverse;
	align-items: center;
	background: rgb(160, 221, 245);
}
.div2 {
	grid-area: 1 / 3 / 2 / 6;
	text-align: left;
	justify-content: center;
	display: flex;
	flex-direction: column;
	/* flex-wrap: wrap; */
	background: rgb(88, 252, 0);
	padding-left: 20px;
}
.div3 {
	grid-area: 2 / 1 / 5 / 3;
	text-align: center;
	display: flex;
	flex-direction: column;
	flex-wrap: wrap;
	background: rgb(160, 221, 245);
	padding: 20px;
}
.div4 {
	grid-area: 2 / 3 / 5 / 6;
	text-align: left;
	display: flex;
	flex-direction: column;
	flex-wrap: wrap;
	padding: 20px;
}

img {
	height: 250px;
	width: auto;
}
.name {
	font-size: 48px;
}
.contact-info {
	font-size: 24px;
}

p {
	font-size: 30px;
	padding-bottom: 30px;
}
a {
	color: black;
	text-decoration: none;
}
a:hover {
	color: rgb(160, 221, 245);
	-webkit-text-fill-color: rgb(160, 221, 245); /* Will override color (regardless of order) */
	-webkit-text-stroke-width: 1px;
	-webkit-text-stroke-color: black;
}
</style>
