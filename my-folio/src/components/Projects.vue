<!-- src/components/Projects.vue -->
<template>
  <section id="projects" class="min-h-screen py-12 bg-white">
    <div class="max-w-7xl mx-auto px-8">
      <h2 class="innovarFont text-4xl md:text-5xl font-bold mb-16 text-black">
        Mes Projets
      </h2>

      <div class="flex flex-col gap-8">
        <a
          v-for="project in projects"
          :key="project.id"
          :href="project.github"
          target="_blank"
          class="relative bg-slate-100 rounded-xl p-4 md:p-8 hover:shadow-xl transition-all duration-300 hover:scale-95 flex flex-col group"
        >
          <div
            class="absolute top-4 right-4 md:top-8 md:right-8 w-10 h-10 md:w-12 md:h-12 bg-black rounded-full flex items-center justify-center"
          >
            <img
              :src="flecheIcon"
              alt=""
              class="w-5 h-5 md:w-6 md:h-6 transition-transform duration-300"
            />
          </div>

          <div class="flex items-center gap-2 md:gap-3 mb-4 md:mb-6">
            <h3 class="Isenheim text-2xl md:text-4xl font-bold text-black">
              {{ project.name }}
            </h3>
          </div>
          <p
            class="Isenheim text-black text-base md:text-lg mb-4 md:mb-6 max-w-lg"
          >
            {{ project.description }}
          </p>
          <div class="flex flex-wrap gap-2 mb-4 md:mb-6">
            <p
              v-for="tech in project.technologies"
              :key="tech"
              class="Isenheim px-2 py-1 md:px-3 md:py-1 text-black rounded-full text-xs md:text-sm font-bold"
            >
              {{ tech }}
            </p>
          </div>

          <div class="mt-auto flex justify-center">
            <div
              class="w-fit max-w-full rounded-lg flex items-center justify-center p-2"
            >
              <img
                :src="project.gif"
                :alt="project.name"
                class="max-w-full h-48 md:h-80 object-cover object-top rounded-md border-2 border-solid border-black"
              />
            </div>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import stanleyjobGif from "../assets/sj-search.gif";
import flecheIcon from "../assets/fleche.png";
import WekaGif from "../assets/WEKA.gif"

const projects = [
  {
    id: 0,
    name: "JobBoard",
    description:
      "JobBoard est une application web permettant de consulter, postuler et administrer des offres d’emploi via une base SQL, une API REST et une interface admin sécurisée.",
    technologies: ["VueJS", "SQL", "Node"],
    github: "https://github.com/Saiile/Jobboard",
    gif: stanleyjobGif,
  },
  {
    id:1,
    name:"WEKA",
    description:
    "Weka est une application web inspirée de Discord qui permet aux utilisateurs de créer et rejoindre des serveurs, d’organiser les conversations en salons, et de profiter d’une interface flexible avec des onglets multiples et déplaçables.",
    technologies: ["Nuxt", "Fastify", "PostgreSQL", "Supabase"],
    github: "https://github.com/Saiile/WEKA",
    gif: WekaGif,
  }
];
</script>

<style scoped>
@font-face {
  font-family: "Innovar";
  src: url("../assets/font/INNOVARELEGANT.ttf") format("truetype");
  font-weight: normal;
  font-style: normal;
}

.innovarFont {
  font-family: "Innovar", sans-serif;
}

@font-face {
  font-family: "isenheim";
  src: url("../assets/font/Isenheim.otf") format("truetype");
  font-weight: normal;
  font-style: normal;
}

.Isenheim {
  font-family: "isenheim", sans-serif;
}
</style>
