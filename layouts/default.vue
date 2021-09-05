<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      dark
      color="primary"
      fixed
      app
    >
      <template #prepend>
        <v-list-item two-line>
          <v-list-item-avatar>
            <v-icon>mdi-account</v-icon>
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>{{ project.name }}</v-list-item-title>
            <v-list-item-subtitle>{{ project.description }}</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </template>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      dark
      color="primary"
      flat
      app
      fixed
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <a href="https://avicenne-agency.com" target="_blank">
        <img height="45" width="45" src="/logo-avicenne.webp">
      </a>
    </v-app-bar>
    <v-main>
      <Nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: true,
      items: [
        {
          icon: 'mdi-rocket-launch',
          title: 'Avancement',
          to: '/'
        },
        {
          icon: 'mdi-chart-gantt',
          title: 'Planning',
          to: '/planning'
        },
        {
          icon: 'mdi-gauge',
          title: 'Heures travaillées',
          to: '/duration'
        },
        {
          icon: 'mdi-monitor-edit',
          title: 'Demandes',
          to: '/request'
        }
      ],
      title: 'Avicenne Agency',
      project: {
        name: 'Grandy\'s',
        description: 'Plateforme de mise en relation & d\'annonces'
      }
    }
  }
}
</script>

<style>
  .v-toolbar__title{
    font-family: 'Gilroy',sans-serif;
    font-weight: bold;
    font-size: 1.4rem;
  }

  .v-list-item__title, .v-list-item__subtitle, .v-list-item__content{
    font-weight: 500;

  }
</style>
