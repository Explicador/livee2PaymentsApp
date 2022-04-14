<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="isDrawerOpen = !isDrawerOpen"
        />

        <q-toolbar-title>
          e2Payments Live Tests
        </q-toolbar-title>

        <div>e2Payments v1.0.0</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="isDrawerOpen"
      show-if-above
      :width="300"
      :breakpoint="400"
    >
      <q-scroll-area style="height: calc(100% - 150px); margin-top: 150px; border-right: 1px solid #ddd">
        <q-list padding>
          <q-item to="/" clickable v-ripple>
            <q-item-section avatar>
              <q-icon name="home" />
            </q-item-section>

            <q-item-section>
              Inicio
            </q-item-section>
          </q-item>

        </q-list>
      </q-scroll-area>

      <q-img class="absolute-top" src="https://explicador.co.mz/wp-content/uploads/2021/07/lagos-techie-IgUR1iX0mqM-unsplash-1-scaled.jpg" style="height: 150px">
        <div class="absolute-bottom bg-transparent">
          <q-avatar size="56px" class="q-mb-sm">
            <img src="https://explicador.co.mz/wp-content/uploads/2021/11/app-icon.png">
          </q-avatar>
          <div class="text-weight-bold">Explicador Inc</div>
          <div>@e2Payments</div>
        </div>
      </q-img>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'MainLayout',
  data () {
    return {
      isDrawerOpen: false
    }
  }
}
</script>
