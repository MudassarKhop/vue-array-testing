<template>
	<div>
		<div class="everything">
			<div id="cards" class="card col-lg-4" style="width: 300px">
				<img v-bind:src="product.image" alt="" />
				<router-link
					:to="{ name: 'cards', params: { id: product.id } }"
					class="card-body"
				>
					<h5 class="card-title">{{ product.title }}</h5>
					<p class="card-text">{{ product.description }}</p>
					<p>
						<i class="fa-solid fa-bolt-lightning"></i>
						{{ product.category }}
					</p>
					<p><i class="fa-solid fa-horse-head"></i> {{ product.company }}</p>
					<p><i class="fa-solid fa-dollar-sign"></i> {{ product.price }}</p>
				</router-link>
			</div>
		</div>
	</div>
</template>
<script>
	export default {
		props: ["product"],
	};
</script>
<style scoped>
	.everything {
		color: black;
	}
	#cards router-link {
		text-decoration: none;
	}
	.card-display {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		justify-content: center;
		align-content: center;
		gap: 50px;
	}
	body {
		background-repeat: no-repeat;
		background-attachment: fixed;
		background-size: 100% 100%;
		backdrop-filter: blur(4px);
	}
	#nav-head {
		margin-left: 12%;
		font-size: 30px;
		font-family: "Racing Sans One", cursive;
		color: white;
		text-shadow: 3px 3px 4px black;
	}
	#nav-foot {
		position: relative;
		left: -65%;
		font-size: 20px;
		font-family: "Racing Sans One", cursive;
		color: white;
		text-shadow: 3px 3px 4px black;
	}
	#nav-foot2 {
		position: relative;
		left: -28%;
	}
	#nav-foot3 {
		position: relative;
		left: 18%;
	}
	.fa-facebook-f {
		color: #232729;
	}
	.fa-instagram {
		color: #232729;
	}
	.fa-at {
		color: #232729;
	}
	.fa-twitter {
		color: #232729;
	}
	.fa-whatsapp {
		color: #232729;
	}
	.fa-facebook-f:hover {
		color: white;
	}
	.fa-instagram:hover {
		color: white;
	}
	.fa-at:hover {
		color: white;
	}
	.fa-twitter:hover {
		color: white;
	}
	.fa-whatsapp:hover {
		color: white;
	}
	#nav-link:hover {
		color: #a4d236;
	}
	.collapse {
		margin-left: 8%;
	}
	.fa-bolt {
		color: #a4d236;
	}
	.fa-phone-volume {
		color: #a4d236;
	}
	.fa-heart {
		color: red;
	}
	.fa-user {
		color: white;
	}
	.fa-user:hover {
		color: #a4d236;
		border: transparent;
	}
	.fa-bolt-lightning {
		color: #a4d236;
	}
	#btn:hover {
		background-color: #a4d236;
		color: white;
		border-radius: 8px;
	}
	#btn2:hover {
		background-color: #a4d236;
		color: white;
		border-radius: 8px;
	}
	.nav-items:hover {
		background-color: #a4d236;
	}

	#btn {
		color: white;
		background-color: transparent;
	}
	#btn2 {
		margin-top: 25px;
	}
	.border-danger {
		color: transparent;
	}
	#landing {
		color: white;
		display: flex;
		flex-direction: column;
		flex-wrap: nowrap;
		justify-content: center;
		align-items: center;
		padding: 12%;
	}

	#P1 {
		text-shadow: 1px 1px 2px black;
	}
	span {
		font-family: "Racing Sans One", cursive;
		color: #a4d236;
		text-shadow: 2px 2px 4px rgb(0, 0, 0);
	}

	#cars {
		background-color: white;
	}
	#sort {
		box-shadow: 20px 20px 60px #000000, -20px -20px 60px #000000;
		height: 20vh;
		margin-bottom: -5%;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;

		margin-left: auto;
		margin-right: auto;
	}
	#heading-cont {
		position: relative;
		bottom: 80%;
	}
	#cards {
		margin-top: 3%;
		margin-right: auto;
		margin-left: auto;
		box-shadow: 1px 1px 2px rgb(0, 0, 0);
	}
	#cards2 {
		margin-right: auto;
		margin-left: auto;
	}
	#footer {
		padding-top: 5%;
		height: 60vh;
		background-color: white;
	}
	#logo {
		display: flex;
		flex-direction: row;
		flex-wrap: nowrap;
		justify-content: center;
		align-items: center;
	}
	#footer1 {
		padding-top: 0%;
		padding: 8%;
		height: 50vh;
		display: flex;
		flex-direction: row;
		flex-wrap: nowrap;
		justify-content: center;
		align-items: center;
		margin-left: auto;
		margin-right: auto;
		background: #a4d236;
	}
	#footer2 {
		height: 10vh;
		display: flex;
		flex-direction: row;
		flex-wrap: nowrap;
		justify-content: center;
		align-items: center;
		margin-bottom: -5%;
		margin-left: auto;
		margin-right: auto;
		background: #6e8c27;
	}
	h2 {
		font-family: "Racing Sans One", cursive;
		text-shadow: 1px 1px 2px rgb(255, 255, 255);
	}
	h5 {
		font-family: "Racing Sans One", cursive;
		text-shadow: 1px 1px 2px rgb(255, 255, 255);
	}
	#missing {
		padding-bottom: 5%;
	}
	option {
		font-family: "Racing Sans One", cursive;
	}
	#cards:hover {
		background-color: white;
		box-shadow: -5px -5px 30px 5px red, 5px 5px 30px 5px blue;
		animation: gloski 0.5s linear infinite;
		transition: box-shadow 1s;
	}
	@keyframes gloski {
		0% {
			box-shadow: -5px -5px 30px 5px crimson, 5px 5px 30px 5px blue;
		}
		50% {
			box-shadow: 5px 5px 30px 5px yellow, -5px -5px 30px 5px purple;
		}
		100% {
			box-shadow: -5px -5px 30px 5px red, 5px 5px 30px 5px blue;
		}
	}

	@media only screen and (max-width: 992px) {
		#nav-head {
			margin-left: 32%;
			font-size: 30px;
			font-family: "Racing Sans One", cursive;
			color: white;
			text-shadow: 3px 3px 4px black;
		}
		#sort {
			box-shadow: 20px 20px 60px #000000, -20px -20px 60px #000000;
			height: 20vh;
			display: flex;
			flex-direction: column;
			flex-wrap: nowrap;
			justify-content: center;
			align-items: center;
			margin-bottom: -5%;
			margin-left: auto;
			margin-right: auto;
		}
		select {
			margin-top: 10%;
		}
		#profile {
			display: none;
		}
	}
</style>
