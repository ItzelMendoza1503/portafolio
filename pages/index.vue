<script setup>
import Background from '~/components/Background.vue'
import AppSideBar from '~/components/AppSideBar.vue'
</script>

<template>
  <Background>

    <AppSideBar />

    <div class="center">
      <div class="card">

        <img src="/imagen yo.jpg" class="profile-img" />

        <h2>Itzel Mendoza</h2>
        <p class="carrera">Ingeniería en Sistemas</p>

        <p><strong>Puesto:</strong> Área de Sistemas / Bases de Datos</p>

        <p><strong>Conocimientos:</strong><br>
        SQL, Bases de datos, Nuxt
        </p>

        <p><strong>Teléfono:</strong> 55 0000 0000</p>

        <p><strong>Correo:</strong> correo@ejemplo.com</p>

      </div>
    </div>

  </Background>
</template>

<style scoped>
.center{
  display:flex;
  justify-content:center;
  align-items:center;
  height:100vh;
}
.profile-img{
  width:120px;
  height:120px;
  border-radius:50%;
  border:3px solid #00ff41;
  margin-bottom:15px;
  object-fit:cover;
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
