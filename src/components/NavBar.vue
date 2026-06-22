<script setup>
defineProps({
  name: {
    type: String,
    required: true
  }
})

const navItems = [
  { label: 'About', href: '#about' },
  { label: 'Projects', href: '#projects' },
  { label: 'Skills', href: '#skills' },
  { label: 'Contact', href: '#contact' }
]
</script>

<template>
  <header class="nav-wrap">
    <nav class="nav container">
      <a href="#top" class="brand">{{ name }}</a>
      <div class="nav-links">
        <a v-for="item in navItems" :key="item.label" :href="item.href">{{ item.label }}</a>
      </div>
    </nav>
  </header>
</template>
