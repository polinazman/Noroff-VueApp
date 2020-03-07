<template>
	<div class="[ row ]">
		<HeadComponent></HeadComponent>
		<div v-for="recipe in recipes" class="[ col-sm-4 ]" v-bind:key="recipe">
			<RecipeComponent v-bind:recImg="recipe.thumbnail"
							v-bind:title="recipe.title"
							v-bind:ingredients="recipe.ingredients"
							v-bind:link="recipe.href"
			></RecipeComponent>
		</div>
	</div>
</template>

<script>
import RecipeComponent from './components/RecipeComponent.vue'
import HeadComponent from './components/HeadComponent.vue'
export default {
	name: 'Recipe',
	components: {
		RecipeComponent, HeadComponent
	},
	data(){
		return{
			recipes: []
		}
	},
	beforeMount: function(){
		const app = this;

		const conversionUrl = 'https://cors-anywhere.herokuapp.com/';
		const url ="http://www.recipepuppy.com/api/";

		fetch(conversionUrl + url)
		.then(function(response) {
			return response.json();
		})
		.then(function(result) {
			app.recipes = result.results;
		})
	}
}
</script>