<script setup lang="ts">
defineProps<{
  id: string;
  data: any[];
  isActive: boolean;
  toggleModal: () => void;
}>()
</script>

<template>
  <section :id="id" class="modal" :class="{'is-active': isActive}">
      <div class="modal-background"></div>
      <div class="modal-content">
        <div class="box">
          <table class="table is-striped is-fullwidth" v-for="(table, index) in data" :key="table.id">
            <thead>
              <tr>
                <th v-for="head in table.head" :key="head.id"><br v-if="index === 0">{{head}}</th>
              </tr>
            </thead>
            <tbody v-if="table.items">
              <tr v-for="tr in table.items" :key="tr.id">
                <td v-for="td in tr" :key="td.id">{{td}}</td>
              </tr>
              </tbody>
          </table>
        </div>
      </div>
      <button @click="toggleModal()" class="modal-close is-large" aria-label="close"></button>
  </section>
</template>