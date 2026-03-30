<!-- src/components/Formation.vue -->
<template>
  <section id="formation" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-8">
      <h2 class="innovarFont text-4xl md:text-5xl font-bold mb-16 text-black">
        Formations
      </h2>

      <div class="max-w-3xl mx-auto relative">
        <div class="absolute left-8 top-0 bottom-0 w-0.5 bg-gray-300"></div>

        <div class="space-y-8">
          <div class="relative pl-20">
            <div
              class="bg-gray-100 rounded-lg p-6 hover:scale-110 transition-all duration-300"
            >
              <p class="Isenheim text-sm text-gray-500 mb-2 block">
                2022 - 2024
              </p>
              <h3 class="Isenheim text-xl font-bold text-black mb-2">
                Webacademie Epitech Strasbourg
              </h3>
              <p class="Isenheim text-gray-700 m-5">
                Formation en développement web avec une approche par projets —
                HTML/CSS, JavaScript, Vue.js, Node.js, bases de données et gestion de projet agile.
              </p>
            </div>
          </div>

          <div class="relative pl-20">
            <div
              class="bg-gray-100 rounded-lg p-6 hover:scale-110 transition-all duration-300"
            >
              <p class="Isenheim text-sm text-gray-500 mb-2 block">
                2025 - 2028
              </p>
              <h3 class="Isenheim text-xl font-bold text-black mb-2">
                Pré-MSC Epitech Montpellier
              </h3>
              <p class="Isenheim text-gray-700 m-5">
                Formation en expertise informatique orientée architecture logicielle,
                management de projet et spécialisation full stack.
              </p>
            </div>
          </div>
        </div>
      </div>

      <h2
        class="innovarFont text-4xl md:text-5xl font-bold mb-16 text-black mt-20"
      >
        Experiences
      </h2>

      <div class="max-w-3xl mx-auto relative">
        <div class="absolute left-8 top-0 bottom-0 w-0.5 bg-gray-300"></div>

        <div class="space-y-8">
          <div class="relative pl-20">
            <div class="bg-gray-100 rounded-lg p-6 hover:scale-110 transition-all duration-300">
              <p class="Isenheim text-sm text-gray-500 mb-2 block">2023 - 2024</p>
              <h3 class="Isenheim text-xl font-bold text-black mb-2">Alternance Developpeur Web</h3>
              <p class="Isenheim text-gray-700">Tech4Gaia - Strasbourg</p>
                <ul class="Isenheim text-gray-700 text-sm space-y-1 list-disc list-inside m-5">
                <li>Développement et amélioration de l'interface utilisateur (UI/UX)</li>
                <li>Correction de bugs front-end et back-end</li>
                <li>Optimisation et correction des appels API</li>
                <li>Participation aux sprints agiles</li>
              </ul>
            </div>
          </div>

          <div class="relative pl-20">
            <div class="bg-gray-100 rounded-lg p-6 hover:scale-110 transition-all duration-300">
              <p class="Isenheim text-sm text-gray-500 mb-2 block">Juil. 2021 - Mars 2022</p>
              <h3 class="Isenheim text-xl font-bold text-black mb-2">Employé Polyvalent</h3>
              <p class="Isenheim text-gray-500 text-sm mb-3">Leclerc — Logelbach</p>
              <ul class="Isenheim text-gray-700 text-sm space-y-1 list-disc list-inside m-5">
                <li>Gestion des encaissements et relation client</li>
                <li>Mise en rayon et optimisation de la présentation produits</li>
                <li>Réapprovisionnement et suivi des stocks</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

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
