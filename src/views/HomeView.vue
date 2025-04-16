<script setup>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Virtual, EffectCube, Pagination } from 'swiper/modules';

import IconArrowRight from '@/components/icons/IconArrowRight.vue';
import IconSend from '@/components/icons/IconSend.vue';
import IconInstagram from '@/components/icons/IconInstagram.vue';
import IconBasketball from '@/components/icons/IconBasketball.vue';
import IconTwitter from '@/components/icons/IconTwitter.vue';
import IconYoutube from '@/components/icons/IconYoutube.vue';

import 'swiper/css/effect-cube'
import 'swiper/css/pagination';

import 'swiper/css'
import '../assets/custom-swiper-bullet.css'

const photo = ref([
  { path: 'Logo1.png', name: 'photo1' },
  { path: 'Logo2.png', name: 'photo2' },
  { path: 'Logo3.png', name: 'photo3' },
  { path: 'Logo4.png', name: 'photo4' },
  { path: 'Logo5.png', name: 'photo5' },
  { path: 'Logo6.png', name: 'photo6' },
  { path: 'Logo7.png', name: 'photo7' }
])


const getImageUrl = (filename) => {
  return new URL(`../assets/image/${filename}`, import.meta.url).href
}
</script>

<template>
  <section id="Hero" class="mx-auto mt-4">
    <Swiper :modules="[Virtual, Pagination]" effect="cube" :loop="true" :grab-cursor="false" :cube-effect="{
      shadow: false,
      slideShadows: false,
      shadowOffset: 20,
      shadowScale: 0.94
    }" :pagination="true">
      <SwiperSlide v-for="i in 3">
        <div class="py-4 px-6 w-full h-[500px] bg-[#F5F7FA]">
          <div
            class="container mx-auto flex md:flex-row md:gap-2 lg:grap-3 xl:gap-4 items-center justify-center w-full h-full">
            <div class="left w-full md:w-1/2 space-y-7">
              <h1 class=" text-xl md:text-3xl lg:text-6xl font-bold">Lessons and insights <br><span
                  class="text-[#4CAF4F]">from 8 years</span></h1>
              <p class="text-lg">Where to grow yout business as a photographer: site or social media?</p>
              <button
                class="px-4 py-3 bg-[#4CAF4F] text-xl font-bold text-white w-[200px] h-[60px] rounded-lg">Register</button>
            </div>
            <div class="right w-1/2 hidden md:block">
              <img src="../assets/image/HeroSection.png" alt="hero_section" class="object-cover mx-auto w-[400px]">
            </div>
          </div>
        </div>
      </SwiperSlide>
    </Swiper>
  </section>

  <section id="Our_clients" class="my-13 h-full md:h-63">
    <div class="container mx-auto px-6">
      <h2 class=" text-xl md:text-3xl lg:text-6xl font-bold text-center text-[#4D4D4D]">Out Clients</h2>
      <p class="text-center mt-6 text-md text-[#717171]">We have been working with some Fortune 500+ clients</p>
      <div class="flex md:flex-row items-center justify-center gap-4 md:gap-30 mt-6">
        <img alt="photo1" class="object-cover w-10 md:w-16 md:h-16" v-for="img in photo" :src="getImageUrl(img.path)">
      </div>
    </div>
  </section>
  <section id="manage">
    <div class="container mx-auto">
      <div class="text-center">
        <h2 class=" text-xl md:text-3xl lg:text-6xl text-[#4D4D4D] font-bold">
          Manage your entire community <br>in a single system
        </h2>
        <p class="text-md text-[#717171] mt-6">Who is Nextcent suitable for?</p>
      </div>
      <div class="my-10 flex flex-col md:flex-row justify-center items-center gap-30">
        <div
          class="w-[400px] h-[300px] md:h-[300px] text-center flex flex-col justify-center items-center shadow-sm px-5 md:px-10 md:py-6">
          <img src="../assets/image/Icon33.png" alt="" class="w-30">
          <h3 class="text-3xl text-[#4D4D4D] font-bold">Membership <br>Organisations</h3>
          <p class="mt-6 text-md text-[#717171]">Our membership management software provider full automation og
            membership renewals and payments</p>
        </div>

        <div
          class="w-[400px] h-[300px] md:h-[300px] text-center flex flex-col justify-center items-center shadow-sm px-5 md:px-10 md:py-6">
          <img src="../assets/image/Icon44.png" alt="" class="w-30">
          <h3 class="text-3xl text-[#4D4D4D] font-bold">National <br>Associations</h3>
          <p class="mt-6 text-md text-[#717171]">Our membership management software provider full automation og
            membership renewals and payments</p>
        </div>

        <div
          class="w-[400px] h-[300px] md:h-[300px] text-center flex flex-col justify-center items-center shadow-sm px-5 md:px-10 md:py-6">
          <img src="../assets/image/Icon55.png" alt="" class="w-30">
          <h3 class="text-3xl text-[#4D4D4D] font-bold">Clubs and<br> Groups</h3>
          <p class="mt-6 text-md text-[#717171]">Our membership management software provider full automation og
            membership renewals and payments</p>
        </div>
      </div>

      <div class="flex flex-col md:flex-row items-center gap-6 space-y-6">
        <div class="w-full md:w-1/2">
          <img src="../assets/image/Frame 35.png" alt="" class="object-cover mx-auto">
        </div>
        <div class="w-full md:w-1/2 px-7">
          <h2 class="text-[#4D4D4D] text-xl md:text-3xl lg:text-6xl font-bold ">The unseen of spending three years at
            Pixelgrade</h2>
          <p class="mt-6 text-[#717171]">Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore sequi in
            accusantium esse laudantium temporibus corporis quibusdam officia ex non earum perspiciatis mollitia beatae
            sapiente pariatur accusamus id, sint quod. Inventore doloremque a atque repudiandae totam, nisi quasi
            molestias nemo repellendus, rerum voluptate officiis facere quo consectetur ea nobis rem!</p>
          <button class="px-4 py-3 mt-2 mb-2 bg-[#4CAF4F] text-white rounded-lg">Learn More</button>
        </div>
      </div>
    </div>
  </section>

  <section id="Helping" class="bg-[#F5F7FA]">
    <div class="container mx-auto ">
      <div class="flex flex-col md:flex-row items-center justify-between w-full md:h-[300px] px-6">
        <div class="">
          <h2 class="text-xl md:text-3xl lg:text-6xl mt-6">Helping a local <br><span class="text-[#4CAF4F]">business
              reinvent
              itself</span></h2>
          <p class="mt-4">We reached here with our hard work and dedication</p>
        </div>
        <div class="grid grid-flow-col grid-rows-2 gap-6 mt-8 mb-7">
          <div class="flex flex-row gap-6 items-center justify-center">
            <img src="../assets/image/Icon (6).png" alt="" class="w-10 md:w-20 -ms-10">
            <div>
              <p>2,245,341</p>
              <p>Members</p>
            </div>
          </div>
          <div class="flex flex-row gap-6 items-center justify-center">
            <img src="../assets/image/Icon (7).png" alt="" class="w-10 md:w-20">
            <div>
              <p>828,867</p>
              <p>Event Bookings</p>
            </div>
          </div>
          <div class="flex flex-row gap-6 items-center justify-center">
            <img src="../assets/image/Icon (8).png" alt="" class="w-10 md:w-20 -ms-6">
            <div>
              <p>46,328</p>
              <p>Clubs</p>
            </div>
          </div>
          <div class="flex flex-row gap-6 items-center justify-center">
            <img src="../assets/image/Icon (9).png" alt="" class="w-10 md:w-20">
            <div>
              <p>1,926,436</p>
              <p>Payments</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="container mx-auto">
      <div class="flex flex-col md:flex-row items-center gap-6 space-y-6">
        <div class="w-full md:w-1/2">
          <img src="../assets/image/pana.png" alt="" class="object-cover mx-auto">
        </div>
        <div class="w-full md:w-1/2 px-7">
          <h2 class="text-[#4D4D4D] text-xl md:text-3xl lg:text-6xl font-bold ">How to design your site footer like we
            did</h2>
          <p class="mt-6 text-[#717171]">Donec a eros justo. Fusce egestas tristique ultrices. Nam tempor, augue nec
            tincidunt molestie, massa nunc varius arcu, at scelerusqye elit erat a magna. Donec quis erat at libero
            ultrices mollis. In hac habitasse platea dictumst. Vivamus vehicula leo dui, at porta hisi facilisis
            finobus. In euismod augue vitae nisi ultricies, non aliquet urna tincidunt. Integer in nisi eget nulla
            commodo faucibus efficitur quis massa. Praesent felis estm finibus et nisi ac, hendrerit venenatis libero.
            Donec cosectetur faucibus ipsum id gravida.</p>
          <button class="px-4 py-3 mt-2 mb-2 bg-[#4CAF4F] text-white rounded-lg">Learn More</button>
        </div>
      </div>
    </div>
  </section>

  <section id="" class="bg-[#F5F7FA]">
    <div class="container mx-auto">
      <div class="flex flex-col md:flex-row items-center gap-6 space-y-6">
        <div class="w-full md:w-1/2">
          <img src="../assets/image/image 9.png" alt="" class="object-cover mx-auto">
        </div>
        <div class="w-full md:w-1/2 px-7">
          <p class="mt-6 text-[#717171]">Maecenas dignissim justo eget nulla rutrum molestie. Maecenas lobortis sem dui,
            vel rutrum risus tincidunt ullamcorper. Proin eu enim metus. Vivamus sed libero ornare, tristique quam in,
            gravida enim. Nullam ut molestie arcu, at hendrerit elit. Morbi laoreet elit at ligula molestie, nec
            molestie mi blandit. Suspendisse cursus tellus sed augue ultrices, quis tristique nulla sodales. Suspendisse
            eget lorem eu turpis vestibulum pretium. Suspendisse potenti. Quisque malesuada enim sapien, vitae placerat
            ante feugiat eget. Quisque vulputate odio neque, eget efficitur libero condimentum id. Curabitur id nibh id
            sem dignissim finibus ac sit amet magna.</p>

          <h4 class="mt-4 text-3xl text-[#4CAF4F] font-bold">Tim Smith</h4>
          <p class="mt-4">Britishg Dragon Boat Racing Associaltion</p>

          <div class="flex md:flex-row gap-3 mt-5">
            <img alt="photo1" class="object-cover w-10 md:w-16 md:h-16 hidden md:block" v-for="i in 6"
              :src="getImageUrl(photo[i].path)">
            <button class="flex flex-row justify-center items-center text-xl text-[#4CAF4F] mb-5 md:mb-0">
              <p>Meet all customers </p>
              <IconArrowRight class="text-sm mt-1.5" />
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="Caring">
    <div class="container mx-auto mt-6 mb-6 px-6">
      <div class="flex flex-col md:flex-row gap-9">
        <div class="relative mb-6 w-full">
          <img src="../assets/image/image 18.png" alt="">
          <div class="bg-[#F5F7FA] md:w-100 h-50 px-6 py-6 absolute -bottom-5 md:left-10 rounded-lg text-center">
            <h4 class="text-[#4D4D4D] text-xl md:text-2xl font-bold">Creating Streamlined Safeguarding Processes with
              OneRen</h4>
            <a href="#"
              class="text-[#4CAF4F] text-2xl flex flex-row gap-3 justify-center items-center text-center mt-4">Readmore
              <IconArrowRight class="text-sm mt-1.5" />
            </a>
          </div>
        </div>
        <div class="relative mb-6 w-full">
          <img src="../assets/image/image 19.png" alt="">
          <div class="bg-[#F5F7FA] md:w-100 h-50 px-6 py-6 absolute -bottom-5 md:left-10 rounded-lg text-center">
            <h4 class="text-[#4D4D4D] text-xl md:text-2xl font-bold">What are your safeguarding responsibilities and how
              can you manage them ?</h4>
            <a href="#"
              class="text-[#4CAF4F] text-2xl flex flex-row gap-3 justify-center items-center text-center mt-4">Readmore
              <IconArrowRight class="text-sm mt-1.5" />
            </a>
          </div>
        </div>
        <div class="relative mb-6 w-full">
          <img src="../assets/image/image 20.png" alt="">
          <div class="bg-[#F5F7FA] md:w-100 h-50 px-6 py-6 absolute -bottom-5 md:left-10 rounded-lg text-center">
            <h4 class="text-[#4D4D4D] text-xl md:text-2xl font-bold">Revamping the Membership Model with Triathlon
              Australia</h4>
            <a href="#"
              class="text-[#4CAF4F] text-2xl flex flex-row gap-3 justify-center items-center text-center mt-4">Readmore
              <IconArrowRight class="text-sm mt-1.5" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="Pellentesque" class="bg-[#F5F7FA]">
    <div class="container mx-auto w-full h-[400px]  flex flex-col justify-center items-center">
      <h3 class="text-2xl md:text-6xl font-bold text-center">Pellentesque suscipit <br> fringilla libero eu.</h3>
      <button
        class="px-4 py-3 mt-10 mb-6 bg-[#4CAF4F] text-white rounded-lg flex flex-row justify-center w-[200px] items-center gap-3">Get
        a Demo
        <IconArrowRight class="text-sm mt-1.5" />
      </button>
    </div>
  </section>

  <footer class="bg-[#151620] h-[900px] md:h-[400px]">
    <div class="container mx-auto">
      <div class="h-[400px] w-full flex flex-col md:flex-row items-center justify-around md:gap-9 md:pt-0 pt-20">
        <div class="left md:ms-9">
          <div class="flex flex-row items-center">
            <div>
              <img src="../assets/image/Icon.png" alt="icon_nav" class="object-cover" width="80" height="80">
            </div>
            <h1 class="text-6xl font-bold text-white ms-2">Nexcent</h1>
          </div>
          <p class="text-white text-xl mt-6 text-center md:text-start">Copyright © 2025 Landify UI Kith.<br> All rights
            reserved</p>
          <div class="flex flex-row items-center justify-center md:justify-start gap-6 text-white mt-6 ">
            <a href="#" class="w-10">
              <IconInstagram class="" />
            </a>
            <a href="#" class="w-10">
              <IconBasketball class="" />
            </a>
            <a href="#" class="w-10">
              <IconTwitter class="" />
            </a>
            <a href="#" class="w-10">
              <IconYoutube class="" />
            </a>
          </div>
        </div>
        <div class="right">
          <div class=" grid md:grid-cols-3 grid-cols-2 gap-15 mt-8 md:gap-2 w-full md:w-[800px]">
            <div class="w-30 ms-6 md:ms-0">
              <h3 class="text-3xl text-white">Company</h3>
              <div class="flex flex-col">
                <a href="#" class="text-xl text-white mt-4">About us</a>
                <a href="#" class="text-xl text-white mt-4">Blog</a>
                <a href="#" class="text-xl text-white mt-4">Contact us</a>
                <a href="#" class="text-xl text-white mt-4">Pricing</a>
                <a href="#" class="text-xl text-white mt-4">Testimonials</a>
              </div>
            </div>
            <div class="w-full">
              <h3 class="text-3xl text-white">Support</h3>
              <div class="flex flex-col">
                <a href="#" class="text-xl text-white mt-4">Help center</a>
                <a href="#" class="text-xl text-white mt-4">Terms of sercvice</a>
                <a href="#" class="text-xl text-white mt-4">Legai</a>
                <a href="#" class="text-xl text-white mt-4">Privacy policy</a>
                <a href="#" class="text-xl text-white mt-4">Status</a>
              </div>
            </div>
            <div class="w-full ms-6 md:ms-0">
              <h3 class="text-3xl text-white w-full">Stay up to date</h3>
              <div class="mt-6 w-[300px]">
                <div
                  class="flex flex-row text-xl items-center justify-between text-white bg-[#263238] py-6 px-6 rounded-xl">
                  <input type="text" placeholder="Your email address " class="text-white focus:outline-none ">
                  <IconSend class="text-[16px]" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>

</template>
