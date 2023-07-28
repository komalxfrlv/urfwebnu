<script setup>
const slides = ref(Array.from({ length: 10 }, () => {
    const r = Math.floor(Math.random() * 256)
    const g = Math.floor(Math.random() * 256)
    const b = Math.floor(Math.random() * 256)
    // Figure out contrast color for font
    const contrast = r * 0.299 + g * 0.587 + b * 0.114 > 186 ? 'black' : 'white'

    return { bg: `rgb(${r}, ${g}, ${b})`, color: contrast }
}))
</script>

<template>
    <section class="services">
        <div>
            <Swiper :height="300" :modules="[SwiperAutoplay, SwiperEffectCreative, SwiperPagination]" :slides-per-view="1"
                :loop="true" :pagination="{ clickable: true }" :effect="'creative'" :autoplay="{
                    delay: 6000,
                    disableOnInteraction: true,
                }" :creative-effect="{
    prev: {
        shadow: false,
        translate: ['-20%', 0, -1]
    },
    next: {
        translate: ['100%', 0, 0]
    }
}">
                <SwiperSlide v-for="(slide, idx) in slides" :key="idx"
                    :style="`background-color: ${slide.bg}; color: ${slide.color};`">
                    {{ idx }}
                </SwiperSlide>
            </Swiper>
        </div>
        <div class="more-services-button">
            Все услуги
        </div>
    </section>
</template>

<style>
.swiper-slide {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 18px;
    height: 60vh;
    font-size: 4rem;
    font-weight: bold;
    font-family: 'Roboto', sans-serif;
}

.swiper-wrapper {
    min-width: 100vh;
    width: 100vh;
}
</style>
<style scoped>
.more-services-button {
    padding: 15px;
    background: #1a73e8;
    color: white;
    text-align: center;
    text-transform: uppercase;
    font-size: 18px;
    font-weight: 300;
    transition: 400ms;
}
.more-services-button:hover {
    background: #1660c2;
}
</style>
