<template >
    <section class="text-white mt-20" id="testimonials" data-aos="zoom-in">
        <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">Testimonials</h2>
        <div class="px-4 xl:px-16">
            <Carousel v-bind="settings" :breakpoints="breakpoints" >
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
    </section>
</template>
<script setup>
import { ref } from 'vue';
import { Carousel , Navigation , Slide } from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';
//Carousel settings
const settings =ref({
    itemsToShow:1,
    snapAlign:"center",
})

//Breakpoints
const breakpoints =ref({
    700:{
        itemsToShow:2.5,
        snapAlign:'center',
    },
    1024:{
        itemsToShow:3,
        snapAlign:'start',
    },
})

const testimonials=ref([
    {
        id:1,
        fullName:'IRUMVA Arsène',
        image:'src/assets/arsene.png',
        comment:'Estimé is a talented web developer who transforms complex challenges into sleek, effective digital solutions. With a sharp design sense and a passion for clean, maintainable code, he stays ahead of the curve. Combining creativity with technical expertise, he builds fast, responsive, and intuitive websites.'
    },
    {
        id:2,
        fullName:'NDAYISENGA Jules César Junior',
        image:'src/assets/cesar.png',
        comment:'Estimé is a talented web developer with a sharp eye for detail and a passion for clean, efficient code. Always up-to-date with the latest tech, he brings creative solutions to every project.'
    },
    {
        id:3,
        fullName:'NIYERA Néré Brunel',
        image:'src/assets/Brunel.png',
        comment:'Estimé is a talented frontend developer with a passion for crafting visually stunning and user-friendly interfaces. With a strong foundation in frontend he brings designs to life with precision and creativity.',
    },
    {
        id:4,
        fullName:'NIKEZWE Marie Prisca',
        image:'src/assets/prisca.png',
        comment:'With a sharp eye for design and detail, Estimé transforms ideas into clean, functional frontend experiences.'
    },
    {
        id:5,
        fullName:'NDABUNGUYE Merci',
        image:'src/assets/merci.png',
        comment:'Estimé turns complex UI concepts into elegant, interactive user experiences using cutting-edge frontend tech.'
    },
])
</script>
<style >
    .carousel__prev,.carousel__next {
        color: white !important;
    }
</style>