<template>
     <v-card
    class="overflow-hidden"
  >
      <v-app-bar
            color="deep-purple"
            dark dense
          >
            <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

            <v-toolbar-title>Title</v-toolbar-title>
          </v-app-bar>
        <v-navigation-drawer
            v-model="drawer"
            fixed
            temporary
          >
            <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            Application
          </v-list-item-title>
          <v-list-item-subtitle>
            subtext
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
          </v-navigation-drawer>
    </v-card>
</template>

<script>
export default {
    name: 'TopBar',
    data: () => ({
        drawer: false,
        group: null,
        items: [
          { title: 'Dashboard', icon: 'mdi-view-dashboard' },
          { title: 'Photos', icon: 'mdi-image' },
          { title: 'About', icon: 'mdi-help-box' },
        ],
        right: null,
    })
}
</script>

<style>

</style>