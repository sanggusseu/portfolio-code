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
        <h2 class="text-h4 text-weight-bold">
          문제를 해결하고 가치를 창출하는 프론트엔드 개발자
        </h2>
        <p>
          저는 학습 과정에서 이론에만 머무르지 않고, 실생활에서 마주한 문제들을
          해결하는 프로젝트를 통해 실전 경험을 쌓아왔습니다.<br />
          특히, iPhone에서 기능이 작동하지 않는 명언 제조기 프로젝트에서 크로스
          브라우징 문제를 해결하고, UI를 개선하여 사용자 혼란을 10명 중 7명에서
          1~2명으로 줄인 경험이 있습니다.<br /><br />
          또한, 노션을 활용하여 업무 정보를 체계화하고, 신규 인력 교육 시간을
          2일에서 1일로 단축하는 등 업무 효율성을 높인 경험도 가지고
          있습니다.<br /><br />
          Vue.js, Quasar, Pinia 등의 기술을 활용해 직관적인 사용자 경험을
          제공하는 애플리케이션 개발에 집중하고 있으며, 앞으로도 실생활 문제를
          해결하며 더 큰 가치를 창출하는 개발자로 성장하고자 합니다.
        </p>
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
