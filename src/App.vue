<template>
  <div id="app" class="page-container md-layout-column">
    <md-app>
      <md-app-toolbar class="md-primary">
        <span class="md-title">News</span>

        <div class="md-toolbar-section-end">
          <md-button @click="showFilter = true">Filter</md-button>
        </div>
      </md-app-toolbar>

      <md-app-drawer class="md-right" :md-active.sync="showFilter">
        <md-app-toolbar class="md-transparent" md-elevation="0">
          <span class="md-title">Filter</span>
        </md-app-toolbar>

        <md-list>
          <md-list-item>
            <span class="md-list-item-text">All</span>
          </md-list-item>

          <md-list-item>
            <span class="md-list-item-text">台灣</span>
          </md-list-item>

          <md-list-item>
            <span class="md-list-item-text">日本</span>
          </md-list-item>
        </md-list>
      </md-app-drawer>

      <md-app-content>
        
        <router-view />
      </md-app-content>
    </md-app>
  </div>
</template>

<script>
export default {
  name: 'App',
   data: () => ({
      showFilter: false
  })
}
</script>

<style>

</style>
