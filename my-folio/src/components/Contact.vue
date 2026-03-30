<!-- src/components/Contact.vue -->
<template>
  <section id="contact" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-8">
      <h2 class="innovarFont text-4xl md:text-5xl font-bold mb-16 text-black">
        Contact
      </h2>
      <p class="Isenheim text-lg md:text-xl">
        Contactez moi pour des nouveaux projet !
      </p>

      <div class="flex flex-col items-center gap-12">
        <div class="bg-white rounded-lg p-8 w-full max-w-lg">
          <form ref="formRef" @submit.prevent="sendEmail" class="space-y-6">
            <div>
              <label class="Isenheim block text-black mb-2 font-medium"
                >Nom</label
              >
              <input
                type="text"
                name="name"
                required
                class="Isenheim w-full px-4 py-3 bg-gray-50 border border-gray-300 rounded-lg text-black focus:outline-none focus:ring-2 focus:ring-black"
                placeholder="Votre nom"
              />
            </div>
            <div>
              <label class="Isenheim block text-black mb-2 font-medium"
                >Email</label
              >
              <input
                type="email"
                name="email"
                required
                class="Isenheim w-full px-4 py-3 bg-gray-50 border border-gray-300 rounded-lg text-black focus:outline-none focus:ring-2 focus:ring-black"
                placeholder="exemple@email.com"
              />
            </div>
            <div>
              <label class="Isenheim block text-black mb-2 font-medium"
                >Message</label
              >
              <textarea
                name="message"
                rows="5"
                required
                class="Isenheim w-full px-4 py-3 bg-gray-50 border border-gray-300 rounded-lg text-black focus:outline-none focus:ring-2 focus:ring-black"
                placeholder="Votre message..."
              ></textarea>
            </div>
            <div class="flex justify-center">
              <button
                type="submit"
                class="Isenheim bg-black hover:bg-gray-800 text-white font-bold py-3 px-6 rounded-lg transition-all duration-300 transform hover:scale-105"
              >
                Envoyer
              </button>
            </div>
          </form>
        </div>

          <div class="flex flex-col sm:flex-row sm:flex-wrap items-start sm:items-center gap-6 text-black">
            
            <!-- Email -->
            <div class="flex items-center gap-3">
              <div class="w-12 h-12 hover:bg-slate-200 transition-all rounded-full flex items-center justify-center" @click="copyMail">
                <img :src="mailIcon" alt="Email" class="w-6 h-6" />
              </div>
              <div>
                <p class="Isenheim text-sm text-gray-500">Email</p>
                <p class="Isenheim hover:text-gray-600 transition-colors" @click="copyMail"> {{ copied ? 'Copié !' : 'elias1.ouissi@epitech.eu' }}</p>
              </div>
            </div>

            <div class="hidden sm:block w-px h-10 bg-gray-300"></div>

            <!-- Github -->
            <div class="flex items-center gap-3">
              <a href="https://github.com/Saiile" target="_blank" rel="noopener noreferrer"
                class="w-12 h-12 hover:bg-slate-200 transition-all rounded-full flex items-center justify-center">
                <img src="../assets/github.png" alt="GitHub" class="w-6 h-6" />
              </a>
              <div>
                <p class="Isenheim text-sm text-gray-500">Github</p>
                <a href="https://github.com/Saiile" target="_blank" class="Isenheim hover:text-gray-600 transition-colors">
                  github.com/Saiile
                </a>
              </div>
            </div>

            <div class="hidden sm:block w-px h-10 bg-gray-300"></div>

            <!-- LinkedIn -->
            <div class="flex items-center gap-3">
              <a href="https://www.linkedin.com/in/elias-ouissi/" target="_blank" rel="noopener noreferrer"
                class="w-12 h-12 hover:bg-slate-200 transition-all rounded-full flex items-center justify-center">
                <img src="../assets/linkedin.png" alt="LinkedIn" class="w-6 h-6" />
              </a>
              <div>
                <p class="Isenheim text-sm text-gray-500">LinkedIn</p>
                <a href="https://www.linkedin.com/in/elias-ouissi/" target="_blank" class="Isenheim hover:text-gray-600 transition-colors">
                  linkedin.com/in/elias-ouissi
                </a>
              </div>
            </div>

          </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import emailjs from "@emailjs/browser";
import mailIcon from "../assets/mail.png";

const formRef = ref(null);
const copied = ref(false)


const sendEmail = (e) => {
  e.preventDefault();

  if (!formRef.value) return;

  emailjs
    .sendForm(
      import.meta.env.VITE_EMAILJS_SERVICE_KEY,
      import.meta.env.VITE_EMAILJS_TEMPLATE_KEY,
      formRef.value,
      import.meta.env.VITE_EMAILJS_PUBLIC_KEY
    )
    .then(
      () => {
        alert("Votre mail a bien été envoyé");
        formRef.value.reset();
      },
      (error) => {
        alert("L'envoi du mail a rencontré une erreur : " + error.text);
      }
    );
};

const copyMail = () => {
  navigator.clipboard.writeText('elias1.ouissi@epitech.eu')
  copied.value = true
  setTimeout(() => copied.value = false, 2000)
}
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
