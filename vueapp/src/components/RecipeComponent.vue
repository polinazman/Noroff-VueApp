<template>
	<div class="[ card ]">
		<div class="[ row ]">
			<div class="[ col-sm-4]"><img :src="recImg" /><br /><br /> <br /></div>
		</div>
			<div class="[ card--information ]"><br />
				<b>Title: </b>{{title}}<br />
				<b>Ingredients: </b>{{ingredients}}<br />
				<b>Link: </b><a href="" v-html="link"></a><br />
			</div>
	</div>
</template>

<script>
export default {
	name: 'RecipeComponent',
	props: ['recImg','title', 'ingredients', 'link'],
}
</script>

<style>
.col-sm-4{
	display: inline-block;
	margin: 20px;
}
.card{
	font-family: "Arial";
	border: solid 1px black;
	border-radius: 4px;
	padding: 0px 20px 30px;
	margin-top: 30px;
	width: 280px;
	height: 320px;
	vertical-align: top;
	display: inline-block;
}

.card img{
	width: auto;
	padding-top: 20px;
}
</style>