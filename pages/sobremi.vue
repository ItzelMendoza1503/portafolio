<script setup>
import Background from '~/components/Background.vue'
import AppSideBar from '~/components/AppSideBar.vue'
</script>

<template>
  <Background>

    <AppSideBar />

    <div class="center">
      <div class="card">

        <h2>Sobre mí</h2>

        <p>
          Soy estudiante de Ingeniería en Sistemas Computacionales con interés en el desarrollo web
          y las bases de datos.
        </p>

        <p>
          Me gusta aprender nuevas tecnologías, resolver problemas y crear proyectos funcionales.
        </p>

        <p>
          Actualmente estoy desarrollando habilidades en programación, diseño web y manejo de bases de datos.
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