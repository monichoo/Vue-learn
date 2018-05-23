<template>
      <v-card>
        <v-toolbar color="orange lighten-1" dark>
          <v-toolbar-side-icon></v-toolbar-side-icon>
          <v-toolbar-title>Open Water</v-toolbar-title>
          <v-spacer></v-spacer>
          <v-btn icon>
            <v-icon>search</v-icon>
          </v-btn>
        </v-toolbar>
        <v-list two-line>
          <template v-for="(item, index) in items">
            <v-subheader
              v-if="item.header"
              :key="item.header"
              inset
            >
              {{ item.header }}
            </v-subheader>
            <v-divider
              v-else-if="item.divider"
              :key="index"
              inset
            ></v-divider>
            <v-list-tile
              v-else
              :key="item.name"
              avatar
              ripple
              @click=""
            >
              <v-list-tile-avatar>
                <img :src="item.avatar">
              </v-list-tile-avatar>
              <v-list-tile-content>
                <v-list-tile-title v-html="item.name"></v-list-tile-title>
                <v-list-tile-sub-title v-html="item.feedback"></v-list-tile-sub-title>
              </v-list-tile-content>
            </v-list-tile>
          </template>
        </v-list>
      </v-card>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            header: 'Open Water'
          },
          { divider: true },
          {
            avatar: 'https://picsum.photos/250/300?image=660',
            name: 'Monica Choo',
            feedback:
              "<span class='text--primary'>Spike Lee</span> &mdash; I'll be in your neighborhood"
          },
          {
            avatar: 'https://picsum.photos/250/300?image=821',
            name: 'Summer BBQ <span class="grey--text text--lighten-1"></span>',
            feedback:
              "<span class='text--primary'>to Operations support</span> &mdash; Wish I could come."
          },
          {
            avatar: 'https://picsum.photos/250/300?image=783',
            name: 'Yes yes',
            feedback:
              "<span class='text--primary'>Bella</span> &mdash; Do you have Paris recommendations"
          },
          {
            header: 'Yesterday'
          },
          { divider: true },
          {
            avatar: 'https://picsum.photos/250/300?image=1006',
            name: 'Dinner tonight?',
            feedback:
              "<span class='text--primary'>Pass</span> &mdash; Do you want to hang out?"
          },
          {
            avatar: 'https://picsum.photos/250/300?image=146',
            name: 'So long',
            subtitle:
              "<span class='text--primary'>Nancy</span> &mdash; Do you see what time it is?"
          },
          {
            header: 'Last Week'
          },
          { divider: true },
          {
            avatar: 'https://picsum.photos/250/300?image=1008',
            name: 'Breakfast?',
            feedback:
              "<span class='text--primary'>LaToya</span> &mdash; Do you want to hang out?"
          },
          {
            avatar: 'https://picsum.photos/250/300?image=839',
            name:
              'Winter Porridge <span class="grey--text text--lighten-1"></span>',
            feedback:
              "<span class='text--primary'>cc: Daniel</span> &mdash; Tell me more..."
          },
          {
            avatar: 'https://picsum.photos/250/300?image=145',
            name: 'Oui oui',
            feedback:
              "<span class='text--primary'>Nancy</span> &mdash; Do you see what time it is?"
          }
        ]
      }
    }
  }
</script>