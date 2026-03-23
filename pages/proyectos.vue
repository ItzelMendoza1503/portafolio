<script setup>
import Background from '~/components/Background.vue'
import AppSideBar from '~/components/AppSideBar.vue'
</script>

<template>
  <Background>

    <AppSideBar />

    <div class="center">
      <div class="card">

        <h2>Proyectos</h2>

        <p><strong>Proyecto 1:</strong><br>
        Página web personal con Nuxt.js
        </p>

        <p><strong>Proyecto 2:</strong><br>
        Sistema básico de base de datos con SQL
        </p>

        <p><strong>Proyecto 3:</strong><br>
        Aplicación web con diseño estilo Matrix
        </p>

        <p>
          Actualmente sigo desarrollando más proyectos para mejorar mis habilidades.
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