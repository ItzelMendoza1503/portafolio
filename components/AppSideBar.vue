<template>
  <div class="menu">
    <NuxtLink to="/">Inicio</NuxtLink>
    <NuxtLink to="/profile">Perfil</NuxtLink>
    <NuxtLink to="/sobremi">Sobre mí</NuxtLink>
    <NuxtLink to="/contactame">Contáctame</NuxtLink>
    <NuxtLink to="/proyectos">Proyectos</NuxtLink>
  </div>
</template>

<style scoped>
.menu{
  position:fixed;
  bottom:20px;
  left:50%;
  transform:translateX(-50%);
  background:#000;
  border:1px solid #00ff41;
  padding:10px 20px;
  display:flex;
  gap:15px;
  box-shadow: 0 0 10px #00ff41;
}

a{
  color:#00ff41;
  text-decoration:none;
  transition:0.3s;
}

a:hover{
  color:#000;
  background:#00ff41;
  padding:5px 10px;
  border-radius:5px;
}
</style>
