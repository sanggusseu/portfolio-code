<template>
  <div class="branch">
    <div class="branch-name">{{ title }}</div>
    <div v-for="(tier, index) in skills" :key="index">
      <SkillTier>
        <SkillBox
          v-for="(skill, i) in tier"
          :key="i"
          :icon="skill.icon"
          :name="skill.name"
          :locked="skill.locked"
        />
      </SkillTier>
    </div>
  </div>
</template>

<script setup>
import SkillBox from './SkillBox.vue';
import SkillTier from './SkillTier.vue';

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  skills: {
    type: Array,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.branch {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 30px;
}

.branch-name {
  font-size: 18px;
  font-weight: bold;
  margin-bottom: 20px;
  text-transform: uppercase;
  letter-spacing: 2px;
  text-shadow: 0 0 5px rgba(255, 255, 255, 0.5);
}
</style>
