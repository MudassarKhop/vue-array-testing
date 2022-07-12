<template>
	<div class="container">
		<div class="display">
			<card v-for="product in products" :key="product.id" :product="product" />
		</div>
	</div>
</template>
<script>
	import Card from "@/components/Card.vue";
	export default {
		components: { Card },
		data() {
			return {
				products: [],
			};
		},
		mounted() {
			fetch(" http://localhost:3000/products")
				.then((res) => res.json())
				.then((data) => (this.products = data))
				.catch((err) => console.log(err.message));
		},
	};
</script>
<style scoped>
	template {
		background-color: black;
	}
	.container {
		height: auto;
		color: rgb(255, 255, 255);
		box-sizing: content-box;
		margin: 0 auto 0 auto;
		border-radius: 4px;
		border: 1px solid rgba(255, 255, 255, 0.5);
		padding: 1rem 1.5rem 2rem 1.5rem;
		backdrop-filter: blur(50px);
		box-shadow: inset 0 -1em 1em rgba(255, 255, 255, 0.1),
			0 0 0 1px rgba(255, 255, 255, 0.1), 0.3em 0.2em 3em rgba(0, 0, 0, 0.2);
	}
	.display {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		justify-content: center;
		align-content: center;
		gap: 25px;
		background-color: black;
	}
</style>
