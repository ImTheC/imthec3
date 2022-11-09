<script setup lang="ts">
import ITCNav from './components/ITCNav.vue';
import ITCMain from './components/ITCMain.vue';
import ITCIntro from './components/ITCIntro.vue';
import ITCTiles from './components/ITCTiles.vue';
import ITCCoder from './components/ITCCoder.vue';
import ITCWriter from './components/ITCWriter.vue';
import ITCActor from './components/ITCActor.vue';
import ITCFooter from './components/ITCFooter.vue';
</script>

<template>
  <ITCNav></ITCNav>
  <ITCMain></ITCMain>
  <section class="container section is-medium">
    <ITCIntro></ITCIntro>
    <ITCTiles></ITCTiles>
  </section>
  <ITCCoder></ITCCoder>
  <ITCWriter></ITCWriter>
  <ITCActor></ITCActor>
  <ITCFooter></ITCFooter>
</template>

<style scoped>

</style>
