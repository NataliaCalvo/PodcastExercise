<script setup>
import { useprincipalStore } from './stores/principalStore'
import HeaderWebpage from './components/HeaderWebpage.vue';
import Podcast from './components/Podcast.vue';

const store = useprincipalStore();

onBeforeMount(async () => {
  await store.fetchPodcast();
  console.log(store.useprincipalStore[0]); 
}),
</script>

<template>
 
    <HeaderWebpage></HeaderWebpage>
    <Podcast></Podcast>

</template>