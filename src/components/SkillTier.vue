<template>
  <div class="tier">
    <div class="horizontal-line"></div>
    <slot></slot>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.tier {
  display: flex;
  justify-content: center;
  margin-bottom: 30px;
  position: relative;
}

.horizontal-line {
  position: absolute;
  top: 50%;
  left: 0;
  right: 0;
  height: 2px;
  background-color: #292928;
  z-index: 0;
}
</style>
