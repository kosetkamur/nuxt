<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" fixed app>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
       <v-row class="mt-10 mb-2 pl-8 widget-left">
        <h4>В нашем роддоме ежедневно рождаются десятки милейших зверушек</h4>
        <img src="@/assets/images/left_widget_img.jpg" alt="animal" width="200">
      </v-row>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: "DefaultLayout",
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Главная",
          to: "/",
        },
        {
          icon: "mdi-apps",
          title: "О нас",
          to: "/about",
        },
        {
          icon: "mdi-apps",
          title: "Запись",
          to: "/form"
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Роддом №5",
    };
  },
 
};
</script>

