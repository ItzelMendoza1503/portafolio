<script setup>
import Background from '~/components/Background.vue'
import AppSideBar from '~/components/AppSideBar.vue'

// Íconos SVG para botones (más modernos que caracteres de texto)
const GithubIcon = `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-github" viewBox="0 0 16 16"> <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.03 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/> </svg>`;

const VercelIcon = `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-triangle-fill" viewBox="0 0 16 16"> <path fill-rule="evenodd" d="M7.022 1.566a1.13 1.13 0 0 1 1.956 0L15.3 12.066c.184.326-.056.734-.43.734H1.13a1.13 1.13 0 0 1-.956-1.734L7.022 1.566z"/> </svg>`;

const projects = [
  {
    title: 'AJEDREZ 3D',
    description: 'Tablero interactivo tridimensional con selección y movimiento de piezas utilizando cargadores geométricos.',
    githubUrl: 'https://github.com/ItzelMendoza1503/ajedrez3D',
    deployUrl: 'https://ajedrez3-d.vercel.app'
  },
  {
    title: 'FIGURA 3D STL',
    description: 'Visualizador web para la manipulación, renderizado y carga de archivos de geometría 3D en tiempo real.',
    githubUrl: 'https://github.com/ItzelMendoza1503/cuarzo3D',
    deployUrl: 'https://cuarzo3-d.vercel.app'
  },
  {
    title: 'PÁGINA API',
    description: 'Catálogo dinámico e-commerce conectado a una API REST para la gestión de productos en tiempo real.',
    githubUrl: 'https://github.com/ItzelMendoza1503/bolsas-de-lujo',
    deployUrl: 'https://bolsas-de-lujo.vercel.app'
  },
  {
    title: 'DESINTEGRADOR DE PARTÍCULAS',
    description: 'Simulador gráfico de físicas con Canvas y animaciones fluidas de dispersión de partículas.',
    githubUrl: 'https://github.com/ItzelMendoza1503/figuras3D',
    deployUrl: 'https://desintegracion-interactiva-3d.vercel.app'
  }
]
</script>

<template>
  <Background>

    <AppSideBar />

    <div class="center">
      <div class="card">

        <h2 class="title">Proyectos Destacados</h2>
        
        <div class="projects-container">
          <div v-for="(project, index) in projects" :key="project.title" class="project-item">
            
            <div class="project-info">
              <span class="project-number">0{{ index + 1 }}</span>
              <strong class="project-title">{{ project.title }}</strong><br>
              <p class="project-desc">{{ project.description }}</p>
            </div>

            <div class="actions-group">
              <a :href="project.githubUrl" target="_blank" rel="noopener" class="btn-github">
                <span class="icon" v-html="GithubIcon"></span>
                GitHub
              </a>
              <a :href="project.deployUrl" target="_blank" rel="noopener" class="btn-vercel">
                <span class="icon" v-html="VercelIcon"></span>
                Vercel
              </a>
            </div>

          </div>
        </div>
        
        <p class="footer-text">
          Actualmente sigo desarrollando más proyectos para mejorar mis habilidades.
        </p>

      </div>
    </div>

  </Background>
</template>

<style scoped>
.center {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  padding: 60px 0;
}

.card {
  background: rgba(18, 18, 18, 0.9);
  border: 1px solid rgba(255, 255, 255, 0.1);
  padding: 40px;
  color: #e0e0e0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; /* Fuente más moderna */
  border-radius: 12px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
  text-align: center;
  max-width: 500px;
  width: 90%;
}

.title {
  margin-top: 0;
  font-size: 1.8rem;
  font-weight: 700;
  color: #fff;
  margin-bottom: 30px;
  letter-spacing: -0.5px;
}

.projects-container {
  text-align: left;
}

.project-item {
  margin-bottom: 40px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  padding-bottom: 20px;
}

.project-item:last-child {
  border-bottom: none;
  margin-bottom: 20px;
}

.project-info {
  margin-bottom: 15px;
  position: relative;
}

.project-number {
  font-size: 1.2rem;
  color: #555;
  font-weight: 700;
  margin-right: 10px;
}

.project-title {
  color: #fff;
  font-size: 1.1rem;
  font-weight: 600;
}

.project-desc {
  color: #b0b0b0;
  font-size: 0.9rem;
  line-height: 1.6;
  margin-top: 8px;
}

/* Grupo de botones */
.actions-group {
  display: flex;
  gap: 15px;
}

/* Botones base */
.btn-github, .btn-vercel {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 10px 16px;
  text-decoration: none;
  font-size: 0.9rem;
  font-weight: 500;
  border-radius: 8px;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.icon {
  display: flex;
  align-items: center;
}

/* Botón GitHub */
.btn-github {
  background: rgba(255, 255, 255, 0.03);
  color: #fff;
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.btn-github:hover {
  background: rgba(255, 255, 255, 0.1);
  box-shadow: 0 4px 12px rgba(255, 255, 255, 0.1);
}

/* Botón Vercel */
.btn-vercel {
  background: rgba(0, 220, 130, 0.05);
  color: #00dc82; /* Verde Nuxt */
  border: 1px solid rgba(0, 220, 130, 0.15);
}

.btn-vercel:hover {
  background: rgba(0, 220, 130, 0.1);
  box-shadow: 0 4px 12px rgba(0, 220, 130, 0.2);
}

.footer-text {
  font-size: 0.85rem;
  color: #888;
  margin-top: 20px;
}
</style>