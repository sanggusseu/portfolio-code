<template>
  <section>
    <q-tabs
      v-model="tab"
      dense
      class="bg-white text-grey-7"
      active-color="primary"
      indicator-color="primary"
      align="start"
    >
      <q-tab name="about" label="About" class="text-capitalize" />
      <q-tab name="projects" label="Projects" class="text-capitalize" />
      <q-tab name="skills" label="Skills" class="text-capitalize" />
      <q-tab name="etc" label="Etc" class="text-capitalize" />
    </q-tabs>

    <q-tab-panels v-model="tab" animated class="bg-white text-dark">
      <q-tab-panel name="about">
        <div class="text-h6">About</div>
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
      </q-tab-panel>

      <q-tab-panel name="projects">
        <ProjectContainer></ProjectContainer>
      </q-tab-panel>

      <q-tab-panel name="skills">
        <SkillTree></SkillTree>
      </q-tab-panel>

      <q-tab-panel name="etc">
        <div class="text-h6">Etc</div>
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
      </q-tab-panel>
    </q-tab-panels>
  </section>
</template>

<script setup>
import { ref } from 'vue';
import SkillTree from './SkillTree.vue';
import ProjectContainer from './ProjectContainer.vue';

const tab = ref('projects');
</script>

<style lang="scss" scoped></style>
