<template>
	<div class="item">
		<div class="item-logo">
			<img :src="image" alt="item">
			<div class="item-logo__text">
				<p class='name'>{{ name }}</p>
				<span>{{ price }}</span>
			</div>
		</div>
		<p>{{ text }}</p>
		<div class="item-footer">
			<div class="actions">
				<div class="bg">
					<svg @click='toggleHeart = !toggleHeart'
				:class="{ 'heart-active': toggleHeart }"
					width="28"
					height="28"
					viewBox="0 0 28 28"
					fill="none"
					xmlns="http://www.w3.org/2000/svg"
				>
					<path
						d="M19.8333 5.25C17.3833 5.25 15.225 6.475 14 8.4C12.775 6.475 10.6167 5.25 8.16667 5.25C4.31667 5.25 1.16667 8.4 1.16667 12.25C1.16667 19.1917 14 26.25 14 26.25C14 26.25 26.8333 19.25 26.8333 12.25C26.8333 8.4 23.6833 5.25 19.8333 5.25Z"
						fill="white"
						fill-opacity="0.38"
					/>
				</svg>
				</div>
				<div class="bg">
					<svg @click='toggleAdd = !toggleAdd'
				:class="{add: toggleAdd}"
					width="30"
					height="30"
					viewBox="0 0 30 30"
					fill="none"
					xmlns="http://www.w3.org/2000/svg"
				>
					<path
						d="M17.5 16.25H16.25V15C16.25 14.6685 16.1183 14.3505 15.8839 14.1161C15.6495 13.8817 15.3315 13.75 15 13.75C14.6685 13.75 14.3505 13.8817 14.1161 14.1161C13.8817 14.3505 13.75 14.6685 13.75 15V16.25H12.5C12.1685 16.25 11.8505 16.3817 11.6161 16.6161C11.3817 16.8505 11.25 17.1685 11.25 17.5C11.25 17.8315 11.3817 18.1495 11.6161 18.3839C11.8505 18.6183 12.1685 18.75 12.5 18.75H13.75V20C13.75 20.3315 13.8817 20.6495 14.1161 20.8839C14.3505 21.1183 14.6685 21.25 15 21.25C15.3315 21.25 15.6495 21.1183 15.8839 20.8839C16.1183 20.6495 16.25 20.3315 16.25 20V18.75H17.5C17.8315 18.75 18.1495 18.6183 18.3839 18.3839C18.6183 18.1495 18.75 17.8315 18.75 17.5C18.75 17.1685 18.6183 16.8505 18.3839 16.6161C18.1495 16.3817 17.8315 16.25 17.5 16.25Z"
						fill="white"
						fill-opacity="0.38"
					/>
					<path
						d="M24.375 8.81249H15.625L12.3375 4.83749C12.2212 4.6941 12.0745 4.57825 11.9081 4.49829C11.7417 4.41832 11.5596 4.37621 11.375 4.37499H5.625C4.80826 4.36496 4.02083 4.67898 3.43512 5.24829C2.84942 5.8176 2.51317 6.59579 2.5 7.41249V22.5875C2.51317 23.4042 2.84942 24.1824 3.43512 24.7517C4.02083 25.321 4.80826 25.635 5.625 25.625H24.375C25.1917 25.635 25.9792 25.321 26.5649 24.7517C27.1506 24.1824 27.4868 23.4042 27.5 22.5875V11.85C27.4868 11.0333 27.1506 10.2551 26.5649 9.68579C25.9792 9.11648 25.1917 8.80246 24.375 8.81249ZM25 22.5625C24.9953 22.6392 24.9753 22.7142 24.9411 22.783C24.9069 22.8518 24.8593 22.9131 24.801 22.9632C24.7427 23.0133 24.675 23.0512 24.6019 23.0747C24.5287 23.0982 24.4515 23.1068 24.375 23.1H5.625C5.54846 23.1068 5.47132 23.0982 5.39815 23.0747C5.32498 23.0512 5.25726 23.0133 5.199 22.9632C5.14073 22.9131 5.0931 22.8518 5.05892 22.783C5.02474 22.7142 5.00471 22.6392 5 22.5625V7.41249C5.00471 7.33578 5.02474 7.2608 5.05892 7.19197C5.0931 7.12315 5.14073 7.06187 5.199 7.01176C5.25726 6.96165 5.32498 6.92373 5.39815 6.90024C5.47132 6.87675 5.54846 6.86816 5.625 6.87499H10.7875L14.0375 10.85C14.1538 10.9934 14.3005 11.1092 14.4669 11.1892C14.6333 11.2692 14.8154 11.3113 15 11.3125H24.375C24.4515 11.3057 24.5287 11.3142 24.6019 11.3377C24.675 11.3612 24.7427 11.3992 24.801 11.4493C24.8593 11.4994 24.9069 11.5606 24.9411 11.6295C24.9753 11.6983 24.9953 11.7733 25 11.85V22.5625Z"
						fill="white"
						fill-opacity="0.38"
					/>
				</svg>
				</div>
			</div>
			<Button>Visit</Button>
		</div>
	</div>
</template>

<script setup>
import Button from './Button.vue';
import { ref } from 'vue';
defineProps({
	image: String,
	price: String,
	name: String,
	text: String,
	id: Number,
})

const toggleHeart = ref(false)
const toggleAdd = ref(false)
</script>

<style lang="scss" scoped>

svg {
	cursor: pointer;
}

.bg {
	background: rgba(255, 110, 48, 0.267);
	width: 42px;
	height: 42px;
	border-radius: 8px;
	display: flex;
	align-items: center;
	justify-content: center;
}

.heart-active path{
	fill: rgb(255, 4, 4);
}

.add path {
	fill: rgb(0, 4, 255);
}

.item {
		p {
			color: #ffffff8c;
		}
		display: flex;
		flex-wrap: wrap;
		flex-direction: column;
		flex: 1 1 400px;
		margin-bottom: 50px;
		gap: 35px;
		height: 300px;
		border-radius: 15px;
		padding: 35px;

		background: rgba(40, 48, 54, 0.6);

		backdrop-filter: blur(25px);

		&-logo {
			display: flex;
			gap: 30px;
			&__text {
				.name {
					font-size: 24px;
					color: #FFFFFFE5;
				}
				span {
					font-size: 18px;
					color: #ffa5378c;
				}
			}
		}

		&-footer {
			display: flex;
			justify-content: space-between;

			.actions {
				display: flex;
				gap: 20px;
			}
		}
	}
</style>
