<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list class="pa-1">
        <v-list-tile avatar>
          <!-- <v-list-tile-avatar>
            <img src="https://randomuser.me/api/portraits/men/85.jpg">
          </v-list-tile-avatar> -->

          <v-list-tile-content>
            <v-list-tile-title>Menu</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>

      <v-list class="pt-0" dense>
        <v-divider></v-divider>

        <v-list-tile
          v-for="item in items"
          :key="item.title"
          @click=""
        >
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>

          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>

    <!-- TOOLBARS -->
    <v-toolbar fixed dark class="light-green darken-1">
    <v-toolbar-side-icon
      @click.stop="drawer = !drawer"
      class="hidden-sm-and-up"
    ></v-toolbar-side-icon>
      <v-toolbar-title>HOTS</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-item class="hidden-xs-only">
        <v-btn flat>
          <v-icon>arrow_forward</v-icon>
          login
        </v-btn>
      </v-toolbar-item>
    </v-toolbar>
    <main>

    </main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: null,
      items: [
        { title: 'login', icon: 'arrow_forward' },
      ]
    }
  },
  // name: 'App'
}
</script>
