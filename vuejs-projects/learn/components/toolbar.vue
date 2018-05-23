<template>
  <v-toolbar dark color="red">
    <v-toolbar-side-icon @click.native.stop="sideNav = ! sideNav"></v-toolbar-side-icon>
    <v-toolbar-title class="white--text">ADA Learn</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn flat>
          <v-icon left>calendar_today</v-icon>
          Calendar
        </v-btn>
        <v-btn flat>
          <v-icon left>people</v-icon>
          Students
        </v-btn>
        <v-btn flat>
          <v-avatar 
              :tile="tile"
              :size="avatarSize"
              color="grey lighten-4"
            >
            <img src="https://yt3.ggpht.com/-V3bet015fWA/AAAAAAAAAAI/AAAAAAAAAAA/iBl8BUarmso/s88-c-k-no-mo-rj-c0xffffff/photo.jpg" alt="avatar">
          </v-avatar>
         </v-btn>
      </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {
  data: () => ({
    slider: 32,
    tile: false
  }),

  computed: {
    avatarSize () {
      return `${this.slider}px`
    }
  }
}
</script>

<--! 
<v-avatar 
            :tile="tile"
            :size="avatarSize"
            color="grey lighten-4"
          >
          <img src="https://yt3.ggpht.com/-V3bet015fWA/AAAAAAAAAAI/AAAAAAAAAAA/iBl8BUarmso/s88-c-k-no-mo-rj-c0xffffff/photo.jpg" alt="avatar">
        </v-avatar>

 -->
 