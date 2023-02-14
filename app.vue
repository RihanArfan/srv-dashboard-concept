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
  </Head>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
