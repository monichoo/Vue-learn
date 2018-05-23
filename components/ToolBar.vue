<template>
    <v-toolbar
      :clipped-left="$vuetify.breakpoint.lgAndUp"
      color="red"
      dark
      app
      fixed
    >
      <v-toolbar-title style="width: 300px" class="ml-0 pl-3">
        <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
        <span class="hidden-xs-and-down" to="/home">ADA Learn</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat to="/calendar" >
          <v-icon left>calendar_today</v-icon>
          Calendar
          </v-btn>
        <v-btn flat to="/students" >
          <v-icon left>people</v-icon>
          Students
        </v-btn>
        <v-btn flat to="/calendar">
          <v-icon left>notifications</v-icon>
          Notifications
        </v-btn>
        <v-btn icon large>
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
 