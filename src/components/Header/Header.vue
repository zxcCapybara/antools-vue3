<template>
	<header>
		<a class="logo" href="#">
			<img src="/src/assets/img/logo.png" alt="logo" />
			<p>antools.</p>
		</a>

		<ul>
			<li><a href="#">Home</a></li>
			<li class="pointer">
				<p>Categories</p>
				<svg
					width="18"
					height="18"
					viewBox="0 0 18 18"
					fill="none"
					xmlns="http://www.w3.org/2000/svg"
				>
					<path
						d="M4.5 6.75L9 11.25L13.5 6.75"
						stroke="white"
						stroke-opacity="0.55"
						stroke-width="1.5"
						stroke-linecap="round"
						stroke-linejoin="round"
					/>
				</svg>
				<ul class="categories">
					<li><a href="#">categories 1</a></li>
					<li><a href="#">categories 2</a></li>
					<li><a href="#">categories 3</a></li>
					<li><a href="#">categories 4</a></li>
				</ul>
			</li>
			<li><a href="#">My Collections</a></li>
			<li><a href="#"></a>Blog</li>
		</ul>

		<div class="registration">
			<button>Login</button>
			<Button>Sign Up</Button>
		</div>
	</header>
</template>
<script setup>
import './header.scss'
import Button from '../Button.vue';
</script>
<style scoped lang="scss"></style>
