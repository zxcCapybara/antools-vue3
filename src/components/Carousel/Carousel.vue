<template>
	<section class="carousel">
		<div class="carousel-item">
			<Carousel v-bind="carouselConfig" :itemsToShow="1">
    <Slide v-for="item in carousel" :key="item">
      <div class="carousel__item">
				<img :src="item.img" alt="">
				<div class="about">
					<p >{{item.name}}</p>
					<span>{{item.post}}</span>
				</div>
				<p class='text'>{{item.text}}</p>
			</div>
    </Slide>

    <template #addons>
      <Navigation />
      <Pagination />
    </template>
  </Carousel>
		</div>
		
	</section>
</template>

<script setup>
import 'vue3-carousel/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
import carousel from '../../js/carousel';

const carouselConfig = {
  itemsToShow: 2.5,
  wrapAround: true
}

import './carousel.scss'
</script>
