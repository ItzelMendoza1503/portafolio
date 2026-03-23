<template>
  <div class="matrix-bg">
    <canvas ref="canvas"></canvas>
    <div class="content">
      <slot />
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue"

const canvas = ref(null)

onMounted(() => {
  const c = canvas.value
  const ctx = c.getContext("2d")

  c.width = window.innerWidth
  c.height = window.innerHeight

  const letters = "01"
  const fontSize = 14
  const columns = c.width / fontSize
  const drops = []

  for (let i = 0; i < columns; i++) {
    drops[i] = 1
  }

  function draw() {
    ctx.fillStyle = "rgba(0,0,0,0.05)"
    ctx.fillRect(0, 0, c.width, c.height)

    ctx.fillStyle = "#00ff41"
    ctx.font = fontSize + "px monospace"

    for (let i = 0; i < drops.length; i++) {
      const text = letters[Math.floor(Math.random() * letters.length)]
      ctx.fillText(text, i * fontSize, drops[i] * fontSize)

      if (drops[i] * fontSize > c.height && Math.random() > 0.975) {
        drops[i] = 0
      }

      drops[i]++
    }
  }

  setInterval(draw, 33)
})
</script>

<style scoped>
.matrix-bg{
  position: relative;
  min-height: 100vh;
  background: black;
}

canvas{
  position: fixed;
  top:0;
  left:0;
  width:100%;
  height:100%;
  z-index:0;
}

.content{
  position: relative;
  z-index:1;
}
</style>