<template>
  <q-page class="q-py-xl q-px-lg">
    <MainContent></MainContent>
  </q-page>
  <TheFooter></TheFooter>
</template>

<script setup>
import TheFooter from 'src/layouts/TheFooter.vue';
import MainContent from 'src/layouts/MainContent.vue';

defineOptions({
  name: 'IndexPage',
});
</script>
