<script setup lang="ts">
useHead({
  title: "Profiles",
});

const profiles = ref([
  {
    id: "a5a0f253-e535-4848-9fa2-ed15e1871c7f",
    name: "Blockgame Panel",
    address: "https://pterodactyl.example.com",
  },
  {
    id: "da97947f-4be8-44db-9f59-31a29a2fd0de",
    name: "Hosting Company",
    address: "https://panel.example.net",
  },
]);
</script>

<template>
  <CardThin class="mb-7 text-center">
    <h2 class="text-2xl font-bold">Link with Pterodactyl</h2>

    <NuxtLink v-slot="{ href }" to="/profiles/add" custom>
      <Button :href="href" type="a" class="mt-5"> Add New Profile </Button>
    </NuxtLink>
  </CardThin>

  <ProfileSummaryCard
    v-for="profile in profiles"
    :key="profile.id"
    class="mb-3"
    :id="profile.id"
    :name="profile.name"
    :address="profile.address"
  />
</template>
