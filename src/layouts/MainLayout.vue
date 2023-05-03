<template>
  <div class="q-pa q-qutter-y-sm">
    <div class="bg-grey text-white">
      <q-toolbar>
        <q-btn flat round dense icon="menu" clsas="q-mr-sm" />
        <q-space />
        <q-btn flat round dense icon="search" class="q-mr-xs" />
      </q-toolbar>
      <q-toolbar inset>
        <q-toolbar-title><strong>Türk</strong> Hisse Senedi Piyasası</q-toolbar-title>
      </q-toolbar>
    </div>
  </div>

  <div class="q-pa-md">
    <q-table flat bordered title="Borsalar" :rows="rows" :columns="columns" row-key="name" dark color="amber" />
  </div>
</template>

<script>
import { defineComponent, ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'



export default defineComponent({
  name: 'MainLayout',

  components: {
  },

  setup() {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
