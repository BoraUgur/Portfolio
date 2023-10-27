<script setup>

import { IconBrandGithub } from '@tabler/icons-vue';
import { IconBrandFacebook } from '@tabler/icons-vue';
import { IconBrandInstagram } from '@tabler/icons-vue';
import { IconMail } from '@tabler/icons-vue';

</script>

<template>
    <div class="w-full h-screen bg-slate-600 relative" id="home">
        <img class="h-full w-full bg-slate-600" src="/resources/bg.jpg" alt="bg.jpg" />
        <h1 class="absolute -left-20 bottom-1/2 text-white text-3xl font-semibold">
            <span>
                Bora Uğur | Sayfama Hoş Geldiniz
            </span>
            <div class="absolute space-x-4 flex mt-5 text-white">
                <a href="https://github.com/BoraUgur">
                    <IconBrandGithub class="w-8 h-8" />
                </a>
                <a href="#">
                    <IconBrandFacebook class="w-8 h-8" />
                </a>
                <a href="#">
                    <IconBrandInstagram class="w-8 h-8" />
                </a>
                <a href="mailto:boraugur47@gmail.com">
                    <IconMail class="w-8 h-8" />
                </a>
            </div>
        </h1>
    </div>

    <div class="h-screen w-full bg-slate-800 bg-opacity-60 text-white px-52 py-10 text-center border-b border-opacity-30 border-slate-400" id="about">

        <div class="overflow-hidden rounded-xl w-3/4 h-1/3 mx-auto">
            <img src="/resources/me.jpg" alt="me.jpg" class="w-full h-full object-cover" />
        </div>

        <h2 class="text-2xl font-semibold my-6">
            Ben Kimim?
        </h2>

        <p class="text-lg w-[90%] mx-auto">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae, minima laboriosam hic repellendus cupiditate,
            error amet tempora non molestias dicta eligendi reiciendis quisquam assumenda placeat ratione, harum adipisci.
            Architecto illum, quaerat voluptatibus tenetur doloremque eligendi corporis sint neque non sed vero maxime,
            explicabo in. Officia nesciunt commodi eveniet laudantium quaerat est at eaque veritatis, non, sapiente atque
            quis. Voluptatibus qui sit dolor. Quo recusandae ipsam, ad nisi illum sit laborum dolor repellendus. Corporis
            praesentium voluptatibus ducimus reprehenderit dignissimos quas ea quis voluptatem voluptas magni sapiente
            doloremque, beatae ex provident dolores qui cupiditate natus, unde atque quo dolorum molestias veniam minima!
        </p>
    </div>
</template>

<style scoped>
h1 {
    transition: all 1.3s ease-in-out;
    animation-name: slideInFromLeft;
    animation-duration: 1.3s;
    animation-timing-function: ease-in-out;
    animation-fill-mode: forwards;
    animation-iteration-count: 1;
}

@keyframes slideInFromLeft {
    0% {
        transform: translateX(0);
    }

    100% {
        transform: translateX(240px);
    }
}</style>