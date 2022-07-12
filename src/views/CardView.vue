<template>
	<div>
		<card v-for="product in products" :key="product.id" :product="product" />
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
<style></style>
