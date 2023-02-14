<template>
  <div class="my-7 flex justify-between gap-2 align-middle">
    <NuxtLink
      to="/"
      class="flex gap-2 rounded-xl p-2 transition-colors hover:bg-neutral-200 dark:hover:bg-neutral-800"
    >
      <img src="/logo.png" alt="SRVControl Logo" class="h-8 w-8 rounded-full" />
      <p class="my-auto text-xl font-semibold">SRVControl</p>
    </NuxtLink>
    <div class="my-auto flex gap-2 pr-2">
      <NuxtLink
        to="https://twitter.com/SRVControl"
        class="h-10 w-10 rounded-full bg-neutral-200 dark:bg-neutral-700"
        target="_blank"
        title="Twitter"
      />
      <NuxtLink
        to="https://discord.gg/7d2s79t"
        class="h-10 w-10 rounded-full bg-neutral-200 dark:bg-neutral-700"
        target="_blank"
        title="Discord"
      />
      <img
        src="https://cdn.discordapp.com/avatars/207629082257653760/5907d628a71a80971db000fceecaab89.png?size=4096"
        alt=""
        class="h-10 w-10 rounded-full bg-neutral-500"
      />
    </div>
  </div>
</template>
