<script setup>

import { ref, onMounted } from 'vue'

const selectedTab = ref('home')

onMounted(() => {
    window.addEventListener('scroll', function () {
        const home = document.querySelector('#home')
        const about = document.querySelector('#about')
        const skills = document.querySelector('#skills')
        const contact = document.querySelector('#contact')

        const homeHeight = home.offsetHeight
        const aboutHeight = about.offsetHeight
        const skillsHeight = skills.offsetHeight
        const contactHeight = contact.offsetHeight

        const scrollPosition = window.scrollY

        if (scrollPosition < homeHeight) {
            selectedTab.value = 'home'
        } else if (scrollPosition < homeHeight + aboutHeight) {
            selectedTab.value = 'about'
        } else if (scrollPosition < homeHeight + aboutHeight + skillsHeight) {
            selectedTab.value = 'skills'
        } else if (scrollPosition < homeHeight + aboutHeight + skillsHeight + contactHeight) {
            selectedTab.value = 'contact'
        }
    })
})

</script>

<template>
    <nav
        class="sticky z-50 top-0 h-16 bg-gray-800 px-4 py-3 w-full flex justify-between items-center text-white text-2xl shadow-sm shadow-slate-500">
        <a href="#" class="px-12 ms-10">
            Bora Uğur
        </a>

        <div class="flex justify-end space-x-8 navbar-links-container px-12 me-10">
            <a href="#home" @click="selectedTab = 'home'" :class="{
                'link-active': selectedTab === 'home'
            }">
                Anasayfa
            </a>
            <a href="#about" @click="selectedTab = 'about'" :class="{
                'link-active': selectedTab === 'about'
            }">
                Hakkımda
            </a>
            <a href="#skills" @click="selectedTab = 'skills'" :class="{
                'link-active': selectedTab === 'skills'
            }">
                Yeteneklerim
            </a>
            <a href="#contact" @click="selectedTab = 'contact'" :class="{
                'link-active': selectedTab === 'contact'
            }">
                İletişim
            </a>
        </div>
    </nav>
</template>

<style scoped>
.navbar-links-container>a {
    position: relative;
    transition: all 0.5s ease-in-out;

    &::after {
        transition: all 0.3s ease-in-out;
        opacity: 0;
        position: absolute;
        top: 2.4rem;
        width: 110%;
        height: 0.2rem;
        left: -5%;
        border-bottom: 3px solid rgb(146, 146, 255);
        content: '';
    }

    &:hover::after {
        opacity: 1;
    }
}

.navbar-links-container>a.link-active::after {
    opacity: 1;
}
</style>