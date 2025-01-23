<template>
	<div class="items">
		<CardTools
			v-for="card in cardsLoaded"
			:key="card.id"
			:image="card.src"
			:id="card.id"
			:name="card.name"
			:price="card.price"
			:text="card.text"
		></CardTools>
		<button @click="loadMore" class="btn-load">Load more</button>
	</div>
</template>

<script setup>
import { computed, ref } from 'vue'
import cardsJS from '../js/cards.js'
import CardTools from './CardTools.vue'
import './ToolsSection/tools.scss'

const cards = ref(cardsJS)

const length = ref(6)

const loadMore = () => {
	if (length.value > cards.value.length) return
	length.value += 6
}

const cardsLoaded = computed(() => cards.value.slice(0, length.value))
</script>

<style lang="scss" scoped></style>
