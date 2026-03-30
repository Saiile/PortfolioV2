<template>
  <section
    id="home"
    class="h-screen flex items-end px-8 pt-20 pb-24 bg-gradient-to-b from-yellow-100 to-white relative"
  >
    <div class="absolute bottom-0 left-1/2 -translate-x-1/2 group">
      <img
        src="../assets/moi.png"
        alt="Moi"
        class="profile-pic w-[90vw] max-w-[450px] h-auto md:w-[500px] lg:w-[600px] object-contain md:grayscale md:group-hover:grayscale-0 md:group-hover:scale-110 transition-all duration-300"
      />
    </div>

    <div
      class="hidden md:block absolute top-8 left-8 z-[60] pointer-events-auto"
    >
      <div
        class="hover:scale-110 transition-transform duration-300 inline-block"
      >
        <a
          href="/CVE.pdf"
          target="_blank"
          download
          class="rounded-full border-2 border-black py-3 px-8 font-semibold text-black hover:bg-black hover:text-white transition-all duration-300"
        >
          CV
        </a>
      </div>
    </div>

    <div class="absolute top-1/2 right-8 -translate-y-1/2 z-[60] pointer-events-auto flex flex-col gap-6">
      <a
        href="https://github.com/Saiile"
        target="_blank"
        rel="noopener noreferrer"
        class="w-12 h-12 rounded-full flex items-center justify-center hover:scale-125 transition-all">
        <img src="../assets/github.png" alt="GitHub" class="w-10 h-10" />
      </a>
      <a
        href="https://www.linkedin.com/in/elias-ouissi/"
        target="_blank"
        rel="noopener noreferrer"
        class="w-12 h-12 rounded-full flex items-center justify-center hover:scale-125 transition-all">
        <img src="../assets/linkedin.png" alt="LinkedIn" class="w-10 h-10" />
      </a>
    </div>

    <div class="absolute top-32 left-8 md:hidden z-10">
      <p class="Isenheim text-lg text-gray-500 leading-relaxed">
        Developpeur Full Stack,<br />
        Etudiant
      </p>
    </div>

    <div class="relative z-10 max-w-4xl">
      <p
        class="hidden md:block Isenheim text-lg md:text-xl text-gray-500 leading-relaxed mb-4 hover:translate-x-5 transition-transform duration-300"
      >
        Developpeur Full Stack,<br />
        Etudiant
      </p>
      <h1
        class="innovarFont text-7xl md:text-8xl lg:text-9xl font-black text-black leading-none mb-8 hover:translate-x-10 transition-transform duration-300"
      >
        Elias Ouissi
      </h1>
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
