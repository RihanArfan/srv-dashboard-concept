<script setup lang="ts">
const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>

<template>
  <div class="my-7 flex items-center justify-between">
    <NuxtLink
      to="/"
      class="flex gap-2 rounded-xl p-2 transition-colors hover:bg-neutral-200 dark:hover:bg-neutral-800"
    >
      <img src="/logo.png" alt="SRVControl Logo" class="h-8 w-8 rounded-full" />
      <p class="my-auto text-xl font-semibold">SRVControl</p>
    </NuxtLink>
    <div class="flex items-center gap-3 pr-2">
      <NavIcon @click="toggleDark()">
        <Icon
          :name="isDark ? 'fa6-solid:sun' : 'fa6-solid:moon'"
          size="1.1em"
        />
      </NavIcon>

      <NuxtLink
        to="https://twitter.com/SRVControl"
        target="_blank"
        title="Twitter"
      >
        <NavIcon><Icon name="fa6-brands:twitter" size="1.1em" /></NavIcon>
      </NuxtLink>
      <NuxtLink to="https://discord.gg/7d2s79t" target="_blank" title="Discord">
        <NavIcon><Icon name="fa6-brands:discord" size="1.3em" /></NavIcon>
      </NuxtLink>

      <img
        src="https://cdn.discordapp.com/avatars/207629082257653760/5907d628a71a80971db000fceecaab89.png?size=4096"
        alt=""
        class="h-10 w-10 rounded-full bg-neutral-500"
      />
    </div>
  </div>
</template>
