<template>
	<section class='main'>
		<div class="description">
			<h6>Awesome tools for Designer & Developer<span>.</span></h6>
			<p>
				Antool is a web collection of information on paid or free Design and
				Development tools
			</p>
			<form action="">
				<input type="text" placeholder="find more than 430+ tools..." />
				<svg
					width="25"
					height="24"
					viewBox="0 0 25 24"
					fill="none"
					xmlns="http://www.w3.org/2000/svg"
				>
					<path
						d="M11 19C15.4183 19 19 15.4183 19 11C19 6.58172 15.4183 3 11 3C6.58172 3 3 6.58172 3 11C3 15.4183 6.58172 19 11 19Z"
						stroke="white"
						stroke-opacity="0.38"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
					/>
					<path
						d="M21 20.9999L16.65 16.6499"
						stroke="white"
						stroke-opacity="0.38"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
					/>
				</svg>
				<Button>Search</Button>
			</form>
			<div class="group">
				<a href="#"
					><img src="/src/assets/img/facebook.png" alt="facebook"
				/></a>
				<a href="#"> <img src="/src/assets/img/insta.png" alt="facebook" /></a>
				<a href="#">
					<img src="/src/assets/img/twitter.png" alt="facebook"
				/></a>
			</div>
		</div>

		<img class="bg" src="/src/assets/img/bg.png" alt="" />
	</section>
</template>

<script setup>
import Button from '../Button.vue'
import './main.scss'
</script>

<style lang="scss" scoped></style>
