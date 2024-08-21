<template>
  <div class="col-12 col-sm-6 col-md-4 col-lg-3">
    <div class="full-width full-height">
      <q-card class="my-card flex column full-height" flat bordered>
        <q-img class="card-img" :src="src" />

        <div class="card-content flex column col-grow">
          <q-card-section class="card-text">
            <div class="text-h5 text-weight-medium q-mt-sm q-mb-xs">
              {{ title }}
            </div>
            <div class="text-h6 text-weight-regular text-grey">
              {{ text }}
            </div>
          </q-card-section>

          <q-card-actions>
            <a
              :href="url"
              target="_blank"
              class="text-primary text-uppercase text-h5 text-weight-medium"
              >Website</a
            >
            <a
              :href="github"
              target="_blank"
              class="text-dark text-uppercase text-h5 text-weight-medium"
              >Github</a
            >

            <q-space />

            <q-btn
              color="grey"
              round
              flat
              dense
              :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
              @click="expanded = !expanded"
            />
          </q-card-actions>
        </div>

        <q-slide-transition>
          <div v-show="expanded">
            <q-separator />
            <q-card-section class="text-h6 text-weight-regular text-grey">
              {{ caption }}
            </q-card-section>
          </div>
        </q-slide-transition>
      </q-card>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const props = defineProps({
  src: String,
  title: String,
  text: String,
  url: String,
  github: String,
  caption: String,
});

const expanded = ref(false);
</script>

<style lang="scss" scoped>
.card-img {
  flex-grow: 0;
}

.card-content,
.card-text {
  flex-grow: 1;
}
</style>
