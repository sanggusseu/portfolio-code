<template>
  <div class="flex full-width">
    <div class="row q-col-gutter-sm col-grow">
      <ProjectCard
        v-for="project in projectList"
        :src="project.src"
        :title="project.title"
        :text="project.text"
        :url="project.url"
        :github="project.github"
        :caption="project.caption"
        :key="project.title"
      ></ProjectCard>
    </div>
  </div>
</template>

<script setup>
import ProjectCard from 'src/components/projects/ProjectCard.vue';

const projectList = [
  {
    src: 'https://sanggusseu.github.io/images/projects/make-quote.jpg',
    title: '명언 제조기',
    text: '어떤 문장이든 명언인 것처럼 보이게 만들어줍니다.',
    url: 'https://sanggusseu.github.io/make-quote/',
    github: 'https://github.com/sanggusseu/make-quote',
    caption:
      'HTML, CSS, JavaScript를 배우고 만들어 본 첫 번째 프로젝트입니다. 검은 배경에 흰색 글자면 명언처럼 보이는 점을 이용한 사이트로, 어떤 문장이든 명언인 것처럼 보이게 만들어 줍니다.',
  },
  {
    src: '',
    title: '멋진 헛간',
    text: '카테고리 별로 사이트를 정리하고 각 사이트에 대한 간단한 설명과 링크를 함께 제공하는 사이트입니다.',
    url: 'https://sanggusseu.github.io/bookmark/',
    github: 'https://github.com/sanggusseu/beautiful-shed',
    caption:
      'Vue 3를 배우기 시작한 초기 단계에서 기본 기능을 익히기 위해 프로젝트를 진행했습니다. 이 과정에서 `v-for`, `props`, `component`, `slot` 등 Vue 3의 핵심 기능을 활용했습니다.',
  },
  {
    src: '',
    title: 'Boggle',
    text: '검색에만 집중할 수 있도록 만든 검색 사이트입니다.',
    url: 'https://sanggusseu.github.io/boggle/',
    github: 'https://github.com/sanggusseu/boggle-code',
    caption:
      'Quasar를 배우고 익숙해지기 위해서 만들어 본 사이트로, 자극적인 콘텐츠에 관심을 뺏기는 일을 방지하고자 만든 심플한 검색 사이트입니다.',
  },
  {
    src: '',
    title: 'CO2 Table Maker',
    text: '맞춤형 CO2 Table을 만들어주는 사이트입니다.',
    url: 'https://sanggusseu.github.io/co2table-maker/',
    github: 'https://github.com/sanggusseu/co2table-maker-code',
    caption:
      'CO2 Table은 이산화탄소 내성을 높이는 훈련 방법 중 하나로, 사용자가 자신의 숨 참기 최고 기록을 입력하면 맞춤형 CO2 Table을 생성해 줍니다. 이 프로젝트에서는 Vue 3 상태 관리 라이브러리인 Pinia를 사용하여 상태 관리를 구현하였습니다.',
  },
  {
    src: '',
    title: '포트폴리오',
    text: '지금 보고 계시는 포트폴리오 사이트입니다.',
    url: 'https://sanggusseu.github.io/',
    github: 'https://github.com/sanggusseu/portfolio-code',
    caption: 'Quasar로 만들었습니다.',
  },
];
</script>

<style lang="scss" scoped></style>
