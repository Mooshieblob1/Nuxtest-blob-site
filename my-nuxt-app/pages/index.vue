<template>
  <div class="back-row-toggle splat-toggle">
    <nav class="bg-transparent p-4 fixed top-0 right-0 w-full">
      <div class="container mx-auto flex justify-end items-center">
        <a
          href="https://blog.mooshieblob.com"
          class="text-white hover:text-gray-400 hover:text-xl hover:font-bold transition duration-300"
        >
          Blog
        </a>
        <a
          href="https://comfy.mooshieblob.com"
          class="text-white hover:text-gray-400 hover:text-xl hover:font-bold transition duration-300"
        >
          ComfyUI
        </a>
      </div>
    </nav>
    <div id="clock" class="clock" />
    <div class="social-links flex">
      <img src="assets/images/bloblogo.webp" alt="" class="social-logo">
      <div class="social-icons flex">
        <a
          href="https://safe.aibooru.online/posts?tags=user%3ABlob"
          target="_blank"
          rel="noopener"
          class="mr-2"
        >
          <img
            src="assets/icons/aibooru.svg"
            alt="AIBooru"
            class="social-icon"
            style="margin-top: 4px"
          >
        </a>
        <a
          href="https://x.com/mooshieblob"
          target="_blank"
          rel="noopener"
          class="mr-2"
        >
          <Icon
            name="pajamas:twitter"
            style="color: #ffcc00; font-size: 35px"
            class="social-icon"
          />
        </a>
        <a
          href="https://github.com/Mooshieblob1/"
          target="_blank"
          rel="noopener"
          class="mr-2"
        >
          <Icon
            name="uil:github"
            style="color: #ffcc00; font-size: 35px"
            class="social-icon"
          />
        </a>
      </div>
    </div>
    <div class="rain front-row" />
    <div class="rain back-row" />
    <img
      id="bg_girl"
      src="assets/images/bg.webp"
      alt="Background Image"
      class="h-4 md:h-6 lg:h-9 w-auto"
    >
    <footer>
      <div class="footer-text">
        <span>© 2024 Mooshieblob</span>
        <a
          id="ipv6"
          href="https://iplocation.io/ipv6-compatibility-checker?url=referer"
        >
          <img
            src="https://iplocation.io/images/ipv6-non-validated.svg"
            alt="ipv6 ready"
            title="ipv6 ready"
            style="border: 0; padding: 0;"
            width="36"
            height="18"
          >
        </a>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { onMounted } from "vue";
import { useHead } from "@vueuse/head";

// SEO Meta Configuration
useHead({
  title: 'Blob',
  meta: [
    { name: 'description', content: 'My links page' },
    { property: 'og:title', content: 'Mooshieblobsite' },
    { property: 'og:description', content: 'My links page' },
    { property: 'og:image', content: '~/assets/images/page.png' },
    { name: 'twitter:card', content: 'summary_large_image' },
  ],
});

// Clock Update Function
onMounted(() => {
  function updateClock() {
    const now = new Date();
    const hours = now.getHours();
    const minutes = now.getMinutes();
    const seconds = now.getSeconds();
    const timeString =
      hours.toString().padStart(2, "0") +
      ":" +
      minutes.toString().padStart(2, "0") +
      ":" +
      seconds.toString().padStart(2, "0");
    const clockElement = document.getElementById("clock");
    if (clockElement !== null) {
      clockElement.textContent = timeString;
    }
  }

  // Call updateClock immediately to set the initial time
  updateClock();

  // Set interval to update the clock every second
  setInterval(updateClock, 1000);
});

// Head Configuration
useHead({
  title: "Mooshieblob",
  meta: [
    { name: "viewport", content: "width=device-width, initial-scale=1.0" },
    { charset: "UTF-8" },
  ],
  link: [
    {
      rel: "stylesheet",
      href: "https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css",
    },
    { rel: "stylesheet", href: "/assets/css/style.css" },
  ],
  script: [
    {
      src: "https://code.jquery.com/jquery-3.7.1.min.js",
      integrity: "sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo=",
      crossorigin: "anonymous",
    },
    {
      src: "https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js",
    },
    { src: "/assets/js/script.js" },
  ],
});
</script>

<style>
/* Your CSS styles here */
</style>
