<script setup>

import { IconBrandVue } from '@tabler/icons-vue';
import { IconBrandLaravel } from '@tabler/icons-vue';
import { IconBrandTailwind } from '@tabler/icons-vue';

</script>

<template>
    <div class="h-screen bg-gray-800 flex px-20 py-16 text-white border-b border-opacity-50 border-slate-300" id="skills">
        <!-- Left -->
        <div class="w-full flex flex-col justify-center items-center space-y-4">
            <div class="w-full text-center space-y-2">
                <h3 class="text-3xl font-semibold">Uzmanlık Alanlarım</h3>
            </div>
            <a class="flex flex-row p-4 rounded-lg min-w-[480px] border-t-8 border-green-500 bg-green-400 bg-opacity-50 cursor-pointer hover:scale-105 transition-all duration-300"
                @click="$emit('setFocusedElement', 'vue')" href="#vue">
                <div class="text-2xl flex space-x-2">
                    <IconBrandVue class="w-8 h-8" />
                    <span>
                        Vue.js
                    </span>
                </div>
            </a>
            <a class="flex flex-row p-4 rounded-lg min-w-[480px] border-t-8 border-green-500 bg-green-400 bg-opacity-50 cursor-pointer hover:scale-105 transition-all duration-300"
                @click="$emit('setFocusedElement', 'laravel')" href="#laravel">
                <div class="text-2xl flex space-x-2">
                    <IconBrandLaravel class="w-8 h-8" />
                    <span>
                        Laravel
                    </span>
                </div>
            </a>
            <a class="flex flex-row p-4 rounded-lg min-w-[480px] border-t-8 border-green-500 bg-green-400 bg-opacity-50 cursor-pointer hover:scale-105 transition-all duration-300"
                @click="$emit('setFocusedElement', 'tailwind')" href="#tailwind">
                <div class="text-2xl flex space-x-2">
                    <IconBrandTailwind class="w-8 h-8" />
                    <span>
                        Tailwind
                    </span>
                </div>
            </a>
        </div>
        <!-- Right -->
        <div class="w-full rounded-lg overflow-hidden">
            <img class="h-full w-full bg-slate-600 object-cover" src="/resources/landscape.jpg" alt="landscape.jpg" />
        </div>
    </div>
</template>