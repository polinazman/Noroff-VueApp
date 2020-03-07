<template>
	<div class="header">
		<img src="../assets/puppy1.png" class="headImg">
		<h1>Recipe Puppy</h1>
		<img src="../assets/puppy2.png" class="headImg">
	</div>
</template>

<script>
export default {
	name: 'HeadComponent'
	}
</script>

<style>
.header {
	margin: 0 auto;
}
.headImg{
	display: inline-block;
	height: 50px;
}

h1{
	display: inline-block;
}
</style>