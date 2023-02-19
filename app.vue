<script setup lang="ts">
useHead({
  titleTemplate: "%s | SRVControl",
  link: [
    { rel: "icon", type: "image/png", href: "/logo.png" },
    { rel: "preconnect", href: "https://fonts.googleapis.com" },
    {
      rel: "preconnect",
      href: "https://fonts.gstatic.com",
      crossorigin: "anonymous",
    },
    {
      rel: "stylesheet",
      href: "https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap",
    },
  ],
});
</script>

<template class="min-h-screen">
  <Head>
    <Body
      class="mx-auto max-w-lg bg-neutral-100 px-3 transition-colors dark:bg-neutral-900 dark:text-neutral-300"
    />
  </Head>

  <Header />

  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
