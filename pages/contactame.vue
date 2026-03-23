<script setup>
import Background from '~/components/Background.vue'
import AppSideBar from '~/components/AppSideBar.vue'
</script>

<template>
  <Background>

    <AppSideBar />

    <div class="center">
      <div class="card">

        <h2>Contáctame</h2>

        <p><strong>Teléfono:</strong><br>
        55 0000 0000
        </p>

        <p><strong>Correo:</strong><br>
        correo@ejemplo.com
        </p>

        <p><strong>Ubicación:</strong><br>
        Ciudad de México
        </p>

        <p>
          Puedes contactarme para proyectos, dudas o colaboración.
        </p>

      </div>
    </div>

  </Background>
</template>

<style scoped>
.center{
  display:flex;
  justify-content:center;
  align-items:center;
  min-height:100vh;
}
.card{
  background: rgba(0,0,0,0.7);
  border: 2px solid #00ff41;
  padding: 30px;
  color: #00ff41;
  font-family: monospace;
  box-shadow: 0 0 20px #00ff41;
  text-align: center;
  max-width:400px;
}
</style>
