<script setup>
import { ref } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Thumbs } from 'swiper';

const thumbsSwiper = ref(null);

const setThumbsSwiper = (swiper) => (thumbsSwiper.value = swiper);

const thumbClasses =
  'border first:rounded-l-md last:rounded-r-md hover:!border-teal-500 not-last:border-r-transparent';
</script>

<template>
  <div class="container py-20">
    <div>
      <Swiper
        :modules="[Thumbs]"
        :slidesPerView="3"
        class="text-center text-sm"
        @swiper="setThumbsSwiper"
      >
        <SwiperSlide :class="thumbClasses">
          <div class="cursor-pointer items-center justify-center px-2 py-4">
            <h2>Lorem</h2>
          </div>
        </SwiperSlide>
        <SwiperSlide :class="thumbClasses">
          <div class="cursor-pointer items-center justify-center px-2 py-4">
            <h2>ipsum</h2>
          </div>
        </SwiperSlide>
        <SwiperSlide :class="thumbClasses">
          <div class="cursor-pointer items-center justify-center px-2 py-4">
            <h2>dolor</h2>
          </div>
        </SwiperSlide>
        <SwiperSlide :class="thumbClasses">
          <div class="cursor-pointer items-center justify-center px-2 py-4">
            <h2>sit</h2>
          </div>
        </SwiperSlide>
        <SwiperSlide :class="thumbClasses">
          <div class="cursor-pointer items-center justify-center px-2 py-4">
            <h2>amet</h2>
          </div>
        </SwiperSlide>
      </Swiper>

      <Swiper
        :modules="[Thumbs]"
        :spaceBetween="30"
        :thumbs="{
          swiper: thumbsSwiper,
          slideThumbActiveClass: 'bg-sky-500 text-white',
        }"
        class="-mx-4 mt-5 overflow-hidden p-4"
      >
        <SwiperSlide class="rounded-lg">
          <img
            class="w-full"
            src="https://picsum.photos/seed/foobar1/400/200"
          />
        </SwiperSlide>
        <SwiperSlide class="rounded-lg">
          <img
            class="w-full"
            src="https://picsum.photos/seed/foobar2/400/200"
          />
        </SwiperSlide>
        <SwiperSlide class="rounded-lg">
          <img
            class="w-full"
            src="https://picsum.photos/seed/foobar3/400/200"
          />
        </SwiperSlide>
        <SwiperSlide class="rounded-lg">
          <img
            class="w-full"
            src="https://picsum.photos/seed/foobar4/400/200"
          />
        </SwiperSlide>
        <SwiperSlide class="rounded-lg">
          <img
            class="w-full"
            src="https://picsum.photos/seed/foobar5/400/200"
          />
        </SwiperSlide>
      </Swiper>
    </div>
  </div>
</template>
