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
        <p class="carrera">Ingeniería en Sistemas Computacionales</p>

        <p><strong>Puesto:</strong><br>
        Área de Sistemas / Bases de Datos
        </p>

        <p><strong>Conocimientos:</strong><br>
        Bases de datos (MySQL), SQL, desarrollo web con Nuxt.js, HTML, CSS y JavaScript
        </p>

        <p><strong>Habilidades:</strong><br>
        Resolución de problemas, trabajo en equipo, aprendizaje rápido y responsabilidad
        </p>

        <p><strong>Descripción:</strong><br>
        Soy estudiante de Ingeniería en Sistemas con interés en el desarrollo web y la gestión de bases de datos. 
        Me gusta crear aplicaciones funcionales y aprender nuevas tecnologías.
        </p>

        <p><strong>Objetivo:</strong><br>
        Desarrollarme profesionalmente en el área de tecnologías de la información y adquirir experiencia en proyectos reales.
        </p>

        <p><strong>Teléfono:</strong><br>
        55 0000 0000
        </p>

        <p><strong>Correo:</strong><br>
        correo@ejemplo.com
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

.carrera{
  margin-bottom:10px;
}
</style>
