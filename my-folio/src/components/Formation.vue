<!-- src/components/Formation.vue -->
<template>
  <section id="formation" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-8">
      <h2 class="innovarFont text-4xl md:text-5xl font-bold mb-16 text-black">
        Formation
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
              <p class="Isenheim text-gray-700">
                Formation en développement web avec une approche par projets.
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
              <p class="Isenheim text-gray-700"></p>
            </div>
          </div>
        </div>
      </div>

      <h2
        class="innovarFont text-4xl md:text-5xl font-bold mb-16 text-black mt-20"
      >
        Experience
      </h2>

      <div class="max-w-3xl mx-auto relative">
        <div class="absolute left-8 top-0 bottom-0 w-0.5 bg-gray-300"></div>

        <div class="space-y-8">
          <div class="relative pl-20">
            <div
              class="bg-gray-100 rounded-lg p-6 hover:scale-110 transition-all duration-300"
            >
              <p class="Isenheim text-sm text-gray-500 mb-2 block">
                2023 - 2024
              </p>
              <h3 class="Isenheim text-xl font-bold text-black mb-2">
                Alternance Developpeur Web
              </h3>
              <p class="Isenheim text-gray-700">Tech4Gaia</p>
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
