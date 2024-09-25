<template>
    <div>
      <nav>
        <div>
          <a href="https://blog.mooshieblob.com">Blog</a>
          <NuxtLink to="/comfy">ComfyUI</NuxtLink>
        </div>
      </nav>
      <footer>
      <div class="footer-text">
        <span>© 2024 Mooshieblob</span>
        <a
          id="ipv6"
          href="https://iplocation.io/ipv6-compatibility-checker?url=referer"
        />
          <img
            src="https://iplocation.io/images/ipv6-non-validated.svg"
            alt="ipv6 ready"
            title="ipv6 ready"
            border="0"
            padding="0"
            width="36"
            height="18"
          >
      </div>
    </footer>
    </div>
  </template>
  
  <script setup>
  import { useHead } from '@vueuse/head';
  
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
  /* Add your styles here */
  </style>
  