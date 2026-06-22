<script setup>
defineProps({
  projects: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <section id="projects" class="section-pad">
    <div class="container">
      <div class="section-heading split">
        <div>
          <p class="eyebrow">Selected work</p>
          <h2>Projects & technical practice</h2>
        </div>
        <p class="section-note">Student projects presented honestly, focused on what I built, practiced, and learned.</p>
      </div>

      <div class="project-list">
        <article v-for="project in projects" :key="project.title" class="project-card">
          <div class="project-top">
            <div>
              <h3>{{ project.title }}</h3>
              <p>{{ project.subtitle }}</p>
            </div>
            <span>{{ project.period }}</span>
          </div>
          <p class="project-desc">{{ project.description }}</p>
          <ul>
            <li v-for="point in project.points" :key="point">{{ point }}</li>
          </ul>
          <div class="tag-row">
            <span v-for="tech in project.stack" :key="tech">{{ tech }}</span>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>
