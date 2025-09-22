<template>
  <section class="text-white mt-20" id="testimonials" data-aos="zoom-in">
    <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">Testimonials</h2>
    <div class="px-4 xl:px-16">
      <div 
        class="relative" 
        @mouseenter="pauseAutoplay" 
        @mouseleave="startAutoplay"
      >
        <Carousel
          ref="carouselRef"
          v-bind="settings"
          :breakpoints="breakpoints"
          :wrapAround="true"
        >
          <Slide v-for="element in testimonials" :key="element.id">
            <div class="carousel__item p-4">
              <div class="w-full mx-auto bg-[#111a3e] shadow-lg border border-[#1f1641] p-5 text-white font-light mb-6">
                <div class="w-full flex mb-4 items-center">
                  <div class="overflow-hidden rounded-full w-10 h-10 bg-gray-50 border border-gray-200">
                    <img :src="element.image" alt="testimonial image" loading="lazy">
                  </div>
                  <h6 class="ml-4 font-bold text-sm uppercase text-white">{{ element.fullName }}</h6>
                </div>
                <div class="w-full">
                  <p class="text-sm leading-tight">
                    <span class="text-lg leading-none italic font-bold text-white mr-1">"</span>
                      {{ element.comment }}
                    <span class="text-lg leading-none italic font-bold text-white mr-1">"</span>
                  </p>
                </div>
              </div>
            </div>
          </Slide>
          <template #addons>
            <Navigation />
          </template>
        </Carousel>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
import { Carousel, Navigation, Slide } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'

// Paramètres
const settings = ref({
  itemsToShow: 1,
  snapAlign: "center",
})

// Responsive breakpoints
const breakpoints = ref({
  700: { itemsToShow: 2.5, snapAlign: 'center' },
  1024: { itemsToShow: 3, snapAlign: 'start' },
})

// Données des témoignages
const testimonials = ref([
  {
    id:1,
    fullName:'IRUMVA Arsène',
    image:'/arsene.png',
    comment:'Estimé is a talented web developer who transforms complex challenges into sleek, effective digital solutions. Combining creativity with technical expertise, he builds fast, responsive, and intuitive websites.'
  },
  {
    id:2,
    fullName:'NDAYISENGA Jules César Junior',
    image:'/cesar.png',
    comment:'Estimé is a talented web developer with a sharp eye for detail and a passion for clean, efficient code. Always up-to-date with the latest tech, he brings creative solutions to every project.'
  },
  {
    id:3,
    fullName:'NIYERA Néré Brunel',
    image:'/Brunel.png',
    comment:'Estimé is a talented frontend developer with a passion for crafting visually stunning and user-friendly interfaces. With a strong foundation in frontend he brings designs to life with precision and creativity.'
  },
  {
    id:4,
    fullName:'NIKEZWE Marie Prisca',
    image:'/prisca.png',
    comment:'With a sharp eye for design and detail, Estimé transforms ideas into clean, functional frontend experiences.'
  },
  {
    id:5,
    fullName:'NDABUNGUYE Merci',
    image:'/merci.png',
    comment:'Estimé turns complex UI concepts into elegant, interactive user experiences using cutting-edge frontend tech.'
  },
  {
    id:6,
    fullName:'NGANJI ALDO ALEX',
    image:'/alex.png',
    comment:'I have rarely worked with a frontend developer as meticulous and creative as Estimé. His code is clean and maintainable.'
  },
  {
    id:7,
    fullName:'HABONIMANA JEAN JUSTE FLEURY',
    image:'/jjf.png',
    comment:'His frontend expertise allows him to turn complex mockups into perfectly interactive experiences.'
  },
])

// Référence du carousel
const carouselRef = ref(null)
let intervalId = null

// Fonction autoplay
const startAutoplay = () => {
  stopAutoplay()
  intervalId = setInterval(() => {
    if (carouselRef.value) {
      carouselRef.value.next() // passe toujours au slide suivant
    }
  }, 3000) // 3s
}

// Stop autoplay
const stopAutoplay = () => {
  if (intervalId) {
    clearInterval(intervalId)
    intervalId = null
  }
}

// Pause au survol
const pauseAutoplay = () => stopAutoplay()

onMounted(() => startAutoplay())
onBeforeUnmount(() => stopAutoplay())
</script>

<style>
.carousel__prev, .carousel__next {
  color: white !important;
}
</style>
