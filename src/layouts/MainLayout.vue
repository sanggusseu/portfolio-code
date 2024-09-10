<template>
  <q-layout view="lHh Lpr lFf">
    <q-header unelevated bordered class="bg-white text-dark">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title class="title text-weight-bold"
          >황상은 포트폴리오</q-toolbar-title
        >
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" bordered>
      <q-list>
        <q-item-label header class="text-h6"> Social Links </q-item-label>

        <EssentialLink
          v-for="social in socialList"
          :key="social.title"
          v-bind="social"
        />
      </q-list>
      <q-list>
        <q-item-label header class="text-h6"> Project Links </q-item-label>

        <EssentialLink
          v-for="project in projectList"
          :key="project.title"
          v-bind="project"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue';
import EssentialLink from 'components/EssentialLink.vue';

defineOptions({
  name: 'MainLayout',
});

const socialList = [
  {
    title: '깃허브',
    caption: 'sanggusseu 깃허브로 이동',
    icon: 'code',
    link: 'https://github.com/sanggusseu',
  },
];

const projectList = [
  {
    title: '명언 제조기',
    caption: '명언처럼 보이게 만들어 주는 사이트',
    icon: 'edit',
    link: 'https://sanggusseu.github.io/make-quote/',
  },
  {
    title: '멋진 헛간',
    caption: '유용한 사이트 모음',
    icon: 'star',
    link: 'https://sanggusseu.github.io/bookmark/',
  },
  {
    title: 'Boggle',
    caption: '검색 사이트',
    icon: 'search',
    link: 'https://sanggusseu.github.io/boggle/',
  },
  {
    title: 'CO2 Table Maker',
    caption: '맞춤형 CO2 Table을 만들어주는 사이트',
    icon: 'waves',
    link: 'https://sanggusseu.github.io/co2table-maker/',
  },
];

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>

<style lang="scss" scoped>
.title {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

@media (min-width: $breakpoint-sm) {
  .title {
    position: static;
    transform: none;
  }
}
</style>
