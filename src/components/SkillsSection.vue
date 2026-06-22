<script setup>
defineProps({
  groups: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <section id="skills" class="section-pad soft-section">
    <div class="container">
      <div class="section-heading">
        <p class="eyebrow">Technical foundation</p>
        <h2>Skills</h2>
      </div>
      <div class="skills-grid">
        <article v-for="group in groups" :key="group.title" class="skill-card">
          <h3>{{ group.title }}</h3>
          <div class="skill-list">
            <span v-for="skill in group.skills" :key="skill">{{ skill }}</span>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>
