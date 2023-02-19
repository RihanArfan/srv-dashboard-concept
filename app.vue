<script setup lang="ts">
useHead({
  titleTemplate: "%s | SRVControl",
});
</script>

<template class="min-h-screen">
  <Head>
    <Link rel="icon" type="image/png" href="/logo.png" />
    <Link rel="preconnect" href="https://fonts.googleapis.com" />
    <Link
      rel="preconnect"
      href="https://fonts.gstatic.com"
      crossorigin="anonymous"
    />
    <Link
      href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap"
      rel="stylesheet"
    />
    <Body
      class="mx-auto max-w-lg bg-neutral-100 px-3 transition-colors dark:bg-neutral-900 dark:text-neutral-300"
    />
  </Head>

  <Header />

  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
