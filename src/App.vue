<script setup>
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import FocusSection from './components/FocusSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import EducationSection from './components/EducationSection.vue'
import ContactSection from './components/ContactSection.vue'
import { profile, focusAreas, projects, skillGroups, education } from './data/portfolio'
</script>

<template>
  <NavBar :name="profile.name" />
  <main>
    <HeroSection :profile="profile" />
    <FocusSection :items="focusAreas" />
    <ProjectsSection :projects="projects" />
    <SkillsSection :groups="skillGroups" />
    <EducationSection :education="education" />
    <ContactSection :profile="profile" />
  </main>
</template>
