<template>
	<span>
		<input type="text" v-model="datum.title" />
		<PureTree v-if="datum.children.length" :data="datum.children" />
	</span>
</template>

<script>
export default {
	name: "pure-leave",
	props: ["datum"],
};
</script>

<style scoped>
input {
  transition: all 200ms ease-out;
	display: block;
	width: 100%;
	height: 30px;
	border-radius: 5px;
	margin-bottom: 10px;
	padding-left: 10px;
	box-sizing: border-box;
}
input[type="text"]:focus {
	background-color: white;

	outline: none;
	/* box-shadow: 0 0 1px 3px rgb(156, 156, 156); */
	/* outline-rad: 1px; */
}
</style>