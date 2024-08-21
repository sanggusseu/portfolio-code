<template>
  <div class="bg">
    <SkillBranch title="Front Skills" :skills="frontSkillList"></SkillBranch>
    <SkillBranch title="Etc Skills" :skills="etcSkillList"></SkillBranch>
  </div>
</template>

<script setup>
import SkillBranch from 'src/components/SkillBranch.vue';

const frontSkillList = [
  [{ icon: 'fa-brands fa-html5', name: 'HTML5' }],
  [
    { icon: 'fa-brands fa-css3-alt', name: 'CSS3' },
    { icon: 'fa-brands fa-js', name: 'JavaScript' },
  ],
  [
    { icon: 'fa-brands fa-vuejs', name: 'Vue' },
    { icon: 'fa-brands fa-react', name: 'React', locked: true },
    { icon: 'fa-solid fa-question', name: '', locked: true },
  ],
];

const etcSkillList = [
  [{ icon: 'fa-brands fa-git-alt', name: 'Git' }],
  [
    { icon: 'fa-brands fa-square-github', name: 'Github' },
    { icon: 'fa-brands fa-figma', name: 'Figma' },
  ],
];
</script>

<style lang="scss" scoped>
.bg {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: rgba(30, 30, 30, 0.8);
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
}
</style>
