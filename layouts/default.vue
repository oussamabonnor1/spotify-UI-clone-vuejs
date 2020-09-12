<template>
  <v-app dark>
    <v-navigation-drawer color="black" permenant app>
      <v-img
        class="ml-4 mt-4 mr-12 mb-6"
        src="https://berndvoss.com/wp-content/uploads/2018/10/spotify-transp-white-1.png"
      ></v-img>
      <v-list nav>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" router exact class="ma-1">
          <v-list-item-action class="mr-4">
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <v-col>
        <span class="text-button text-uppercase grey--text ml-2">Playlists</span>
        <v-list-item class="pl-2">
          <v-list-item-action class="mr-4">
            <v-icon>mdi-plus</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Create Playlist</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item class="pl-2">
          <v-list-item-action class="mr-4">
            <v-icon>mdi-heart</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Liked Songs</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider class="ml-2 mt-2"></v-divider>
        <v-list-item class="pl-2">
          <v-list-item-action class="mr-4">
            <v-icon>mdi-download-circle-outline</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Install App</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-col>
      <v-img
        class="fill-width"
        src="https://images-na.ssl-images-amazon.com/images/I/61Uxg-SWExL._SL1500_.jpg"
      ></v-img>
    </v-navigation-drawer>
    <v-app-bar flat style="background:#121212" app>
      <v-row>
        <v-btn icon>
          <v-icon large>mdi-arrow-left-bold-circle</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon dark large>mdi-arrow-right-bold-circle</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <v-chip close close-icon="mdi-menu-down" class="mt-2 grey darken-3">
          <v-avatar left>
            <v-icon >mdi-account-circle</v-icon>
          </v-avatar>
          <span class="mr-2 font-weight-bold">SageModeBoy</span>
        </v-chip>
      </v-row>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt /> 
      </v-container>
    </v-main>
    <v-footer app fixed>
      <MusicPlayer></MusicPlayer>
    </v-footer>
  </v-app>
</template>

<script>
import MusicPlayer from "@/components/music_player"
export default {
  components:{
    MusicPlayer
  },
  data() {
    return {
      items: [
        {
          icon: "mdi-home",
          title: "Home",
          to: "/"
        },
        {
          icon: "mdi-magnify",
          title: "Search",
          to: "/search"
        },
        {
          icon: "mdi-playlist-music",
          title: "Your library",
          to: "/library"
        }
      ]
    };
  }
};
</script>

<style>
</style>