<template>
<button @click="toggleTheme" class="theme-toggle-btn">
  Cambiar modo
</button>
</template>

<script setup>
const colorMode = useColorMode()

const toggleTheme = () => {
  colorMode.preference = colorMode.value === 'dark' ? 'light' : 'dark'
}
</script>
