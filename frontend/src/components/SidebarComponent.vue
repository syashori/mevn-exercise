<template>
      <v-app-bar
        color="primary"
        prominent
      >
        <v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title to="/home" >MEVN Exercise</v-toolbar-title>
        
      </v-app-bar>

      <v-navigation-drawer
        v-model="drawer"
        location="left"
        permanent
      >
      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.link" link>
          <v-list-item-title>{{item.title}}</v-list-item-title>
        </v-list-item>
      </v-list>
      </v-navigation-drawer>
</template>

<script>
  export default {
    data: () => ({
      drawer: false,
      group: null,
      items: [
        {
          title: 'Dashboard',
          link:"/dashboard"
        },
        {
          title: 'Project',
          link:"/project"
        },
        {
          title: 'Login',
          value: 'bar',
          link:"/login"
        },
        {
          title: 'Logout',
        },
      ],
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
  }
</script>