<script setup>
defineProps({
  items: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <section class="section-pad soft-section">
    <div class="container">
      <div class="section-heading">
        <p class="eyebrow">Career direction</p>
        <h2>What I am working toward</h2>
      </div>
      <div class="focus-grid">
        <article v-for="item in items" :key="item.title" class="focus-card">
          <h3>{{ item.title }}</h3>
          <p>{{ item.text }}</p>
        </article>
      </div>
    </div>
  </section>
</template>
