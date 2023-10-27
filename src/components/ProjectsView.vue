<script setup>

defineProps({
    focusedElement: String,
    scrolled: Boolean
})

</script>

<template>
    <div class="py-16 px-20 min-h-screen text-white">
        <h1 class="text-3xl font-bold mb-16">Yapmış Olduğum Projeler</h1>

        <div class="hidden" id="vue"></div>
        <div class="hidden" id="laravel"></div>
        <div class="hidden" id="tailwind"></div>

        <div class="flex space-x-6 w-full justify-center">
            <div class="flex flex-col bg-slate-700 bg-opacity-90 rounded-lg min-w-[360px] min-h-[250px] overflow-hidden border-l-2 border-green-500"
                :class="{
                    'ring-2 ring-violet-500 ring-opacity-80': focusedElement === 'vue',
                    'card-animation': scrolled,
                    'card': !scrolled,
                }">
                <div class="bg-slate-600">
                    <img class="w-full h-32 object-contain" src="/resources/vue-logo.png" alt="vue-logo.png" />
                </div>
                <div class="p-3 space-y-3">
                    <h3 class="font-semibold text-lg mb-4">Vue.js</h3>

                    <div class="px-4 py-3 bg-slate-800 bg-opacity-50 rounded-lg border-l-8 border-emerald-400">
                        Lorem ipsum dolor sit amet consectetur
                    </div>
                    <div class="px-4 py-3 bg-slate-800 bg-opacity-50 rounded-lg border-l-8 border-emerald-400">
                        Lorem ipsum dolor sit amet consectetur
                    </div>
                    <div class="px-4 py-3 bg-slate-800 bg-opacity-50 rounded-lg border-l-8 border-emerald-400">
                        Lorem ipsum dolor sit amet consectetur
                    </div>
                </div>
            </div>

            <div class="flex flex-col bg-slate-700 bg-opacity-90 rounded-lg min-w-[360px] min-h-[250px] overflow-hidden border-l-2 border-green-500"
                :class="{
                    'ring-2 ring-violet-500 ring-opacity-80': focusedElement === 'laravel',
                    'card-animation': scrolled,
                    'card': !scrolled,
                }">
                <div class="bg-slate-600">
                    <img class="w-full h-32 object-cover" src="/resources/laravel-logo.jpg" alt="laravel-logo.jpg" />
                </div>
                <div class="p-3 space-y-3">
                    <h3 class="font-semibold text-lg mb-4">Laravel</h3>

                    <div class="px-4 py-3 bg-slate-800 bg-opacity-50 rounded-lg border-l-8 border-teal-400">
                        Lorem ipsum dolor sit amet consectetur
                    </div>
                    <div class="px-4 py-3 bg-slate-800 bg-opacity-50 rounded-lg border-l-8 border-teal-400">
                        Lorem ipsum dolor sit amet consectetur
                    </div>
                    <div class="px-4 py-3 bg-slate-800 bg-opacity-50 rounded-lg border-l-8 border-teal-400">
                        Lorem ipsum dolor sit amet consectetur
                    </div>
                </div>
            </div>

            <div class="flex flex-col bg-slate-700 bg-opacity-90 rounded-lg min-w-[360px] min-h-[250px] overflow-hidden border-l-2 border-green-500"
                :class="{
                    'ring-2 ring-violet-500 ring-opacity-80': focusedElement === 'tailwind',
                    'card-animation': scrolled,
                    'card': !scrolled,
                }">
                <div>
                    <img class="w-full h-32 object-fill" src="/resources/tailwind-logo.svg" alt="tailwind-logo.svg" />
                </div>
                <div class="p-3 space-y-3">
                    <h3 class="font-semibold text-lg mb-4">Tailwind</h3>

                    <div class="px-4 py-3 bg-slate-800 bg-opacity-50 rounded-lg border-l-8 border-green-400">
                        Lorem ipsum dolor sit amet consectetur
                    </div>
                    <div class="px-4 py-3 bg-slate-800 bg-opacity-50 rounded-lg border-l-8 border-green-400">
                        Lorem ipsum dolor sit amet consectetur
                    </div>
                    <div class="px-4 py-3 bg-slate-800 bg-opacity-50 rounded-lg border-l-8 border-green-400">
                        Lorem ipsum dolor sit amet consectetur
                    </div>
                </div>
            </div>
        </div>

        <div class="project-gallery">
            <div>
                <img src="/resources/project-1.jpg" alt="">
            </div>
            <div>
                <img src="/resources/project-2.jpg" alt="">
            </div>
            <div>
                <img src="/resources/project-3.jpg" alt="">
            </div>
            <div>
                <img src="/resources/project-4.jpg" alt="">
            </div>
            <div>
                <img src="/resources/project-5.jpg" alt="">
            </div>
            <div>
                <img src="/resources/project-6.jpg" alt="">
            </div>
        </div>

    </div>
</template>

<style>
.card {
    transform: scaleY(0.025);
}

@media (prefers-reduced-motion: no-preference) {
    .card-animation {
        animation: wipe-enter 1.3s 1;
    }
}

@keyframes wipe-enter {
    0% {
        transform: scaleY(0.025);
    }

    50% {
        transform: scaleY(1);
    }
}

.project-gallery {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;

    margin: 2rem 0;
    padding: 1.4rem;
    --_bg-color: #39475c;
    background-color: var(--_bg-color);
    box-shadow: 0 0 0 100vmax var(--_bg-color);
    clip-path: inset(0 -100vmax);
}

.project-gallery>* {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 0.5rem;
    overflow: hidden;
}

.project-gallery>*>* {
    transition: all 0.3s ease-in-out;
}

.project-gallery>*>*:hover {
    transform: scale(1.05);
}

html {
    scroll-behavior: smooth;
}
</style>