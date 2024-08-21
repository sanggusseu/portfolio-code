<template>
  <div class="skill" :class="locked && 'locked'">
    <div class="skill-icon">
      <i :class="icon" aria-hidden="true"></i>
    </div>
    <div class="skill-name">{{ name }}</div>
  </div>
</template>

<script setup>
const props = defineProps({
  icon: String,
  name: String,
  locked: Boolean,
});
</script>

<style lang="scss" scoped>
.skill {
  width: 80px;
  height: 80px;
  background-color: #2a2a2a;
  border: 2px solid #444;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 0 15px;
  cursor: pointer;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.skill.locked {
  background-color: #1a1a1a;
  border-color: #333;
  cursor: not-allowed;
}

.skill.locked .skill-name,
.skill.locked .skill-icon {
  opacity: 0.3;
}

.skill:hover:not(.locked) {
  transform: scale(1.1);
  box-shadow: 0 0 15px rgba(255, 255, 255, 0.3);
}

.skill-icon {
  color: white;
  font-size: 24px;
  margin-bottom: 5px;
}

.skill-name {
  color: white;
  font-size: 10px;
  text-align: center;
  opacity: 0.7;
}
</style>
