
<template>
	<ul>
		<li v-for="leave in data" :key="leave.id">
			<pure-leave :datum="leave"></pure-leave>
		</li>
	</ul>
</template>

<script>
export default {
	name: "pure-tree",
	props: ["data"],
};
</script>

<style scoped>
ul {
	display: block;
	border-radius: 10px;
	box-sizing: border-box;
	padding: 0px !important;
	list-style: none;
}
li {
	background-color: rgb(216, 216, 216);
	border: 5px solid rgb(226, 226, 226);
	box-shadow: 0 6px 10px 0 #00000040;
	box-sizing: border-box;
	padding: 15px !important;

	border-radius: 8px;
}

li:last-child {
	margin-top: 25px;
}
li:first-child {
	margin-top: 0;
}
</style>