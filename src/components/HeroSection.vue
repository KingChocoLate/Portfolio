<script setup>
import profileImage from '../assets/profile.jpg'

defineProps({
  profile: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <section id="top" class="hero section-pad">
    <div class="container hero-grid">
      <div class="hero-copy">
        <p class="eyebrow">Open to AI / software engineering opportunities</p>
        <h1>{{ profile.name }}</h1>
        <p class="headline">{{ profile.headline }}</p>
        <p id="about" class="summary">{{ profile.summary }}</p>

        <div class="fact-row">
          <span v-for="fact in profile.quickFacts" :key="fact">{{ fact }}</span>
        </div>

        <div class="hero-actions">
          <a class="btn primary" :href="`mailto:${profile.email}`">Email Me</a>
          <a class="btn secondary" href="#projects">View Projects</a>
        </div>
      </div>

      <aside class="profile-card">
        <img :src="profileImage" :alt="`${profile.name} portrait`" />
        <div>
          <h2>{{ profile.role }}</h2>
          <p>{{ profile.location }}</p>
        </div>
        <div class="contact-mini">
          <a :href="`mailto:${profile.email}`">{{ profile.email }}</a>
          <a :href="`tel:${profile.phone}`">{{ profile.phone }}</a>
        </div>
      </aside>
    </div>
  </section>
</template>
