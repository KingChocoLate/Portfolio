<script setup>
defineProps({
  education: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <section class="section-pad">
    <div class="container education-card">
      <div class="section-heading">
        <p class="eyebrow">Education</p>
        <h2>{{ education.degree }}</h2>
      </div>
      <div class="education-info">
        <p>{{ education.school }}</p>
        <p>{{ education.status }} · {{ education.period }}</p>
      </div>
      <div class="course-row">
        <span v-for="course in education.courses" :key="course">{{ course }}</span>
      </div>
    </div>
  </section>
</template>
