<template>
  <v-app>
    <TopBar/>
  <!-- Sizes your content based upon application components -->
  <v-main>
    <!-- Provides the application the proper gutter -->
    <v-container fluid>
      <Tyt/>
    </v-container>
  </v-main>

  <BottomBar/>
  </v-app>
</template>

<script>
import BottomBar from './components/BottomBar.vue';
import TopBar from './components/TopBar.vue';
import Tyt from './components/Tyt.vue';

export default {
  name: 'App',

  components: {
    Tyt,
    TopBar,
    BottomBar,
  },
  data: () => ({
   
  }),
};
</script>
