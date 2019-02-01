<template>
  <v-app>
    <v-navigation-drawer app permanent fixed :width="200">
      <v-toolbar flat>
        <v-list>
          <v-list-tile>
            <v-list-tile-title class="title">
              <router-link to="/home">Sample</router-link>
            </v-list-tile-title>
          </v-list-tile>
        </v-list>
      </v-toolbar>

      <v-divider></v-divider>

      <v-list dense class="pt-0">
        <v-list-tile
          v-for="item in items"
          :key="item.title"
        >
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>

          <v-list-tile-content>
            <router-link to="/about">Go to about</router-link>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>



    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data () {
    return {
      items: [
        { title: 'Clients', icon: 'dashboard' },
        { title: 'Matters', icon: 'dashboard' },
        { title: 'Objects', icon: 'dashboard' },
        { title: 'Search', icon: 'search' },
        { title: 'Reports', icon: 'question_answer' }
      ]
    }
  }
}
</script>
