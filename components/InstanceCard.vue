<script setup lang="ts">
const props = defineProps<{
  id: string;
  name: string;
  address: string;
}>();

const hostname = computed(() => new URL(props.address).hostname);
</script>

<template>
  <Card
    class="flex p-5 transition-colors hover:bg-neutral-300 dark:hover:bg-neutral-700"
  >
    <img
      src="@/assets/pterodactyl.png"
      :alt="`${name} Instance Icon`"
      class="mr-5 hidden h-16 w-16 rounded-lg sm:block"
    />
    <div class="my-auto grow">
      <p class="text-lg font-bold">{{ name }}</p>
      <p class="lowercase">{{ hostname }}</p>
    </div>

    <NuxtLink v-slot="{ href }" :to="`/profiles/${id}`" custom>
      <Button :href="href" type="a" class="my-auto">Manage →</Button>
    </NuxtLink>
  </Card>
</template>
