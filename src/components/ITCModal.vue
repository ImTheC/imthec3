<script setup lang="ts">
defineProps<{
  id: string;
  data: string;
  imgData: {
    src: string;
    alt: string;
  };
  isActive: boolean;
  toggleModal: () => void;
}>()
</script>

<template>
  <section :id="id" class="modal" :class="{'is-active': isActive}">
    <div class="modal-background"></div>
    <div class="modal-content">
      <div class="box hero has-text-centered">
        <img class="image image-bump modal-image height" :src="imgData.src" :alt="imgData.alt">
        <div v-html="data"></div>
      </div>
    </div>
    <button @click="toggleModal()" class="modal-close is-large" aria-label="close"></button>
  </section>
</template>