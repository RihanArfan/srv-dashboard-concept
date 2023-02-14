<script setup lang="ts">
useHead({
  titleTemplate: "%s | SRVControl",
});

const isDark = useDark();
const toggleDark = useToggle(isDark);
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
      class="mx-auto min-h-screen max-w-lg bg-neutral-100 px-3 transition-colors dark:bg-neutral-900 dark:text-neutral-300"
    />
  </Head>
  <div class="flex min-h-screen flex-col">
    <Header />
    <div class="flex-1">
      <NuxtLayout>
        <NuxtPage />
      </NuxtLayout>
    </div>
    <div class="my-5 flex justify-center">
      <button
        class="h-10 w-10 rounded-xl border border-neutral-400 p-2 dark:border-neutral-600"
        @click="toggleDark()"
      >
        {{ isDark ? "☀️" : "🌙" }}
      </button>
    </div>
  </div>
</template>
