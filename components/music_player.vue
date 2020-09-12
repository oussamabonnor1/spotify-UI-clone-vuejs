<template>
  <v-row justify="space-between" align="center" class="mr-2">
    <v-col>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title>The Promised Neverland Opening Full</v-list-item-title>
          <v-list-item-subtitle>By UVERworld</v-list-item-subtitle>
        </v-list-item-content>
        <v-list-item-action class="ml-2">
          <v-btn color="#1CB04A" icon>
            <v-icon>mdi-heart</v-icon>
          </v-btn>
        </v-list-item-action>
        <v-list-item-action>
          <v-btn color="grey" icon>
            <v-icon>mdi-dock-window</v-icon>
          </v-btn>
        </v-list-item-action>
      </v-list-item>
    </v-col>
    <v-spacer></v-spacer>
    <v-col>
      <v-row justify="center">
        <v-btn color="grey" icon class="mx-2">
          <v-icon>mdi-shuffle</v-icon>
        </v-btn>
        <v-btn color="grey" icon class="mx-2">
          <v-icon>mdi-skip-previous</v-icon>
        </v-btn>
        <v-btn color="grey" icon class="mx-2">
          <v-icon x-large>mdi-play-circle-outline</v-icon>
        </v-btn>
        <v-btn color="grey" icon class="mx-2">
          <v-icon>mdi-skip-next</v-icon>
        </v-btn>
        <v-btn color="grey" icon class="mx-2">
          <v-icon>mdi-repeat</v-icon>
        </v-btn>
      </v-row>
      <div style="width:500px;">
        <v-slider hide-details color="#1CB04A" v-model="volume" min="0" max="100" readonly>
          <template v-slot:prepend>0:28</template>
          <template v-slot:append>3:15</template>
        </v-slider>
      </div>
    </v-col>
    <v-spacer></v-spacer>
    <v-col>
      <v-row>
        <v-btn color="grey" icon class="mr-2">
          <v-icon>mdi-playlist-play</v-icon>
        </v-btn>
        <v-btn color="grey" icon class="mr-2">
          <v-icon>mdi-monitor-cellphone-star</v-icon>
        </v-btn>

        <div style="width:150px;">
          <v-slider dense hide-details color="grey" v-model="volume" min="0" max="100">
            <template v-slot:prepend>
              <v-icon color="grey">mdi-volume-high</v-icon>
            </template>
          </v-slider>
        </div>
      </v-row>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    volume: 50,
  }),
};
</script>

<style>
</style>