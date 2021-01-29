<template>
    <v-navigation-drawer
      v-model="drawer"
      app
      dark
      color="grey darken-3"
    >
     <v-list-item class="mb-10 mt-10 d-flex justify-center">
         <v-icon x-large>mdi-android-studio</v-icon>
      </v-list-item>
      <v-list>
        <v-list-item-group
        v-model="selectedItem"
        color="red">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          active-class="border"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

</template>

<script>
  export default {
    data: () => ({ 
        drawer: null,
        selectedItem: 1,
      items: [
        { text: 'DASHBOARD', icon: 'mdi-view-dashboard' },
        { text: 'PROJECTS', icon: 'mdi-briefcase-check' },
        { text: 'MY TASK', icon: 'mdi-menu' },
        { text: 'CALENDAR', icon: 'mdi-calendar' },
        { text: 'TIME MANAGE', icon: 'mdi-clock' },
        { text: 'REPORTS', icon: 'mdi-chart-pie' },
        { text: 'SETTINGS', icon: 'mdi-cog-outline' },
      ],
        }),
  }
</script>
<style scoped>
.border {
  border-right: 5px solid red;
}
</style>