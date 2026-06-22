<script setup>
defineProps({
  profile: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <section id="contact" class="section-pad contact-section">
    <div class="container contact-card">
      <div>
        <p class="eyebrow">Contact</p>
        <h2>Let’s connect</h2>
        <p>I am ready to learn, contribute carefully, and grow through real technical work.</p>
      </div>
      <div class="contact-actions">
        <a class="btn primary" :href="`mailto:${profile.email}`">{{ profile.email }}</a>
        <a class="btn secondary" :href="`tel:${profile.phone}`">{{ profile.phone }}</a>
      </div>
    </div>
  </section>
</template>
