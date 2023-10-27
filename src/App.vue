<script setup>

import NavbarView from './components/NavbarView.vue'
import FooterView from './components/FooterView.vue'
import AboutMeView from './components/AboutMeView.vue'
import SkillsView from './components/SkillsView.vue'
import ProjectsView from './components/ProjectsView.vue'
import ContactView from './components/ContactView.vue'

import { ref, onMounted } from 'vue'

const focusedElement = ref('')
const scrolledToProjects = ref(false)

function setFocusedElement(element) {
  focusedElement.value = element
}

onMounted(() => {
  window.addEventListener('scroll', () => {
    if (window.scrollY > 1000) {
      scrolledToProjects.value = true
    }
  })
})

</script>

<template>
  <div class="bg-gray-800">
    <NavbarView />

    <AboutMeView />
    <SkillsView :focusedElement="focusedElement" @setFocusedElement="setFocusedElement" />
    <ProjectsView :focusedElement="focusedElement" :scrolled="scrolledToProjects" />
    <ContactView />

    <FooterView />
  </div>
</template>