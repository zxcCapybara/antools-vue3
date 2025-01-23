<template>
	<section class="comer-tools">
		<div class="company">
			<p>Trusted more than 150+ brand</p>
			<div class="company-list">
				<a :href="item.src" v-for="item in company">
					<img :src="item.url" alt="" />
				</a>
			</div>
		</div>
		<div class="comer-tools__item">
			<div class="comer-tools__item-text">
				<h1>Newcomer Tools</h1>
				<span
					>Wow! see the latest update of the most recommended tools from
					reliable designers and developers</span
				>
				<Button class=".btn">Explore more</Button>
			</div>
			<div class="comer-tools__item-cards">
				<CardTools
					v-for="card in cards.slice(6, 10)"
					:key="card.id"
					:image="card.src"
					:id="card.id"
					:name="card.name"
					:price="card.price"
					:text="card.text"
				></CardTools>
			</div>
		</div>
	</section>
</template>

<script setup>
import cards from '../../js/cards';
import Button from '../Button.vue'
import CardTools from '../CardTools.vue'
import './newComerTools.scss'

import company from '/src/js/companyList.js'
</script>
