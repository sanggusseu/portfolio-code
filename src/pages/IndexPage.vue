<template>
  <q-page class="full-width flex justify-center">
    <div class="container q-py-xl q-px-lg">
      <UserProfile></UserProfile>
      <MainContent></MainContent>
    </div>
  </q-page>
  <TheFooter></TheFooter>
</template>

<script setup>
import TheFooter from 'src/layouts/TheFooter.vue';
import MainContent from 'src/layouts/MainContent.vue';
import UserProfile from 'src/components/UserProfile.vue';

defineOptions({
  name: 'IndexPage',
});
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  max-width: 140rem;
}
</style>
