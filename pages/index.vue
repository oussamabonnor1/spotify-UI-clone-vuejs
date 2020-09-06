<template>
  <div>
    <v-row>
      <span class="text-h5 font-weight-bold">Recently Played</span>
      <v-spacer></v-spacer>
      <span class="caption grey--text mr-2">SEE ALL</span>
    </v-row>
    <v-row class="mt-5">
      <v-card rounded v-for="item in musicList()" :key="item.title" class="ma-2">
        <v-img :src="item.img" height="145" width="145" class="mx-4 mt-4"></v-img>
        <v-card-title>{{item.title}}</v-card-title>
        <v-card-subtitle class="mb-6">{{item.author}}</v-card-subtitle>
      </v-card>
    </v-row>
    <v-row class="mt-12">
      <v-col class="pa-0">
        <div class="text-h5 font-weight-bold mb-1">Made for SageModeBoy</div>
        <div class="grey--text">Get better recommendations the more you listen.</div>
      </v-col>
      <v-spacer></v-spacer>
      <span class="caption grey--text mr-2">SEE ALL</span>
    </v-row>
    <v-row class="mt-5">
      <v-card rounded v-for="item in musicList()" :key="item.title" class="ma-2">
        <v-img :src="item.img" height="145" width="145" class="mx-4 mt-4"></v-img>
        <v-card-title>{{item.title}}</v-card-title>
        <v-card-subtitle class="mb-6">{{item.author}}</v-card-subtitle>
      </v-card>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    music: [
      {
        title: "Daily Mix",
        author: "By Spotify",
        img:
          "https://ph-files.imgix.net/cbbf111b-fccf-48a7-8505-bedc7b5d5272?auto=format"
      },
      {
        title: "Daily Mix 2",
        author: "By Spotify",
        img: "https://i.redd.it/avxncpgy8do11.png"
      },
      {
        title: "Billie Eilish Radio",
        author: "Billie Eilish",
        img: "https://i1.sndcdn.com/artworks-000596082951-jpphgp-t500x500.jpg"
      },
      {
        title: "Today's Top Hits",
        author: "By Spotify",
        img:
          "https://i.pinimg.com/474x/75/28/e7/7528e70aef7cf03be7a5fb13a163f476.jpg"
      },
      {
        title: "Teen Party",
        author: "By Spotify",
        img:
          "https://i.pinimg.com/236x/54/79/44/54794436b71840391593e0eedf63f782.jpg"
      },
      {
        title: "Soft Pop Hits",
        author: "By Spotify",
        img:
          "https://i.pinimg.com/236x/3a/2a/c3/3a2ac3ff768e01b8c3d10ccea5e52725.jpg"
      }
    ]
  }),
  methods:{
    musicList(){
      const newArr = this.music.slice()
        for (let i = newArr.length - 1; i > 0; i--) {
            const rand = Math.floor(Math.random() * (i + 1));
            [newArr[i], newArr[rand]] = [newArr[rand], newArr[i]];
        }
        return newArr
    }
  }
};
</script>
