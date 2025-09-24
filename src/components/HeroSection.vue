<template>
    <section class="relative w-full" data-aos="zoom-in-up">
        <div class="absolute top-0 inset-x-0 h-64 flex items-start">
            <div class="h-24 w-2/3 bg-gradient-to-br from-[#570cac] blur-2xl invisible opacity-40"></div>
            <div class="h-20 w-3/5 bg-gradient-to-r from-[#670ccf] opqcity-40 blur-2xl"></div>
        </div>
        <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-screen-lg lg:max-w-screen-xl mx-auto relative">
            <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 relative pt-24 lg:max-w-none max-w-2xl md:max-w-3xl mx-auto">
                <div class="lg:py-6">
                    <div class="text-center lg:text-left">
                        <h1 class="pt-4 text-white font-bold text-4xl md:text-5xl lg:text-6xl">
                            Hi, I'm <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-pink-500">
                                BAZAYO Estimé Ninon
                            </span>
                        </h1>
                    </div>
                    <p class="text-gray-300 pt-8 text-center lg:text-left mx-auto max-w-xl">
                        I am a passionate front-end developer specializing in creating modern and high-performance web interfaces. With expertise in HTML, CSS and JavaScript. I bring designs to life with precision and creativity.
                    </p>
                    <div class="flex items-center gap-3 pt-9 flex-col sm:flex-row sm:w-max sm:mx-auto lg:mx-0">
                        
                        <!-- Bouton CV -->
                        <button class=" border border-primary px-6 md:px-7 py-3 rounded-full relative group w-full sm:w-max flex justify-center">
                            <div class="hover:scale-105 transition-all ease-in-out flex justify-center items-center relative">
                                <div class="svg-container">
                                    <svg class="download-icon" width="18" height="22" viewBox="0 0 18 22" fill="none" xmlns="http://www.w3.org/2000/svg" >
                                        <path class="download-arrow" d="M13 9L9 13M9 13L5 9M9 13V1" stroke="#f59e0b"
                                        stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                                        />
                                        <path d="M1 17V18C1 18.7956 1.31607 19.5587 1.87868 20.1213C2.44129
                                        20.6839 3.20435 21 4 21H14C14.7956 21 15.5587 20.6839 16.1213
                                        20.1213C16.6839 19.5587 17 18.7956 17 18V17"
                                        stroke="#f59e0b" stroke-width="2" stroke-linecap="round" />
                                    </svg>
                                    <div class="download-loader text-white hidden"></div>
                                </div>
                                <a href="/resume.pdf" download="resume.pdf" class="pl-2 text-primary"> Download my CV</a>
                            </div>
                        </button>

                        <!-- Bouton GitHub -->
                        <a href="https://github.com/Bazagod" target="_blank" rel="noopener noreferrer"
                           class="flex items-center gap-2 border border-gray-500 px-6 md:px-7 py-3 rounded-full hover:bg-gray-800 transition-all ease-in-out w-full sm:w-max justify-center">
                            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor"
                                 class="text-white" viewBox="0 0 24 24">
                                <path fill-rule="evenodd" clip-rule="evenodd"
                                      d="M12 .297C5.373.297 0 5.67 0 12.297c0 5.292 3.438 
                                      9.787 8.205 11.387.6.113.82-.262.82-.582 
                                      0-.288-.01-1.05-.015-2.06-3.338.726-4.042-1.61-4.042-1.61-.546-1.387-1.333-1.757-1.333-1.757-1.09-.745.083-.73.083-.73 
                                      1.205.084 1.84 1.237 1.84 1.237 1.07 1.834 2.807 
                                      1.304 3.492.997.108-.775.418-1.305.76-1.605-2.665-.3-5.466-1.334-5.466-5.93 
                                      0-1.31.468-2.382 1.236-3.222-.124-.303-.536-1.523.118-3.176 
                                      0 0 1.008-.322 3.3 1.23.96-.267 1.986-.4 
                                      3.006-.405 1.02.005 2.047.138 
                                      3.006.405 2.291-1.552 3.297-1.23 
                                      3.297-1.23.656 1.653.244 2.873.12 
                                      3.176.77.84 1.235 1.912 1.235 
                                      3.222 0 4.61-2.803 5.625-5.475 
                                      5.922.43.372.823 1.102.823 2.222 
                                      0 1.606-.014 2.898-.014 3.293 
                                      0 .322.218.699.825.58C20.565 22.08 
                                      24 17.586 24 12.297 24 5.67 18.627.297 12 .297z"/>
                            </svg>
                            <span class="text-white">Visit my GitHub</span>
                        </a>
                    </div>
                </div>
                <div class="lg:h-full md:flex">
                    <div class="flex w-full h-96 min-h-[24rem] lg:min-h-[none] lg:w-full lg:h-full items-center relative">
                        <div class="absolute z-0 top-1/2 -translate-y-1/2 w-5/6 right-0 h-[calc(80%+20px)] bg-gradient-to-tr opacity-25 from-[#570cac] to-primary blur-2xl"></div>
                        <div class="absolute h-full z-10 p-2 -translate-y-1/2 top-1/2 lg:right-3 md:right-40 sm:right-16 rounded-full shadow-lg border border-primary">
                            <img src="@/assets/Bazagod.jpg" alt="Hero pic" width="500" height="auto" loading="lazy"
                            class="w-full h-full rounded-full object-cover"
                            >
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import AOS from 'aos';
import 'aos/dist/aos.css';
AOS.init();
</script>
