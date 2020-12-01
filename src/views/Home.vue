<template>
  <v-container>
      <v-card width="400" style="margin: 0 auto;">
        <v-img
          height="200px"
          src="https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg"
        >
          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
          >
            <v-app-bar-nav-icon color="white"></v-app-bar-nav-icon>

            <v-toolbar-title class="title white--text pl-0">
              Messages
            </v-toolbar-title>

            <v-spacer></v-spacer>

            <v-btn
              color="white"
              icon
            >
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </v-app-bar>

          <v-card-title class="white--text mt-8">
            <v-avatar size="56">
              <img
                alt="user"
                src="https://cdn.pixabay.com/photo/2020/06/24/19/12/cabbage-5337431_1280.jpg"
              >
            </v-avatar>
            <p class="ml-3">
              Joker Won
            </p>
          </v-card-title>
        </v-img>

        <v-card-text>
          <div class="font-weight-bold ml-8 mb-2">
            Today
          </div>

          <v-timeline
            align-top
            dense
          >
            <v-timeline-item
              v-for="message in messages"
              :key="message.time"
              :color="message.color"
              small
            >
              <div>
                <div class="font-weight-normal">
                  <strong>{{ message.from }}</strong> @{{ message.time }}
                </div>
                <div>{{ message.message }}</div>
              </div>
            </v-timeline-item>
          </v-timeline>
        </v-card-text>
      </v-card>
  </v-container>
</template>

<script>

export default {
  name: 'Home',
  data() {
    return {
      messages: [
        {
          id: 5,
          time: '11:20pm',
          color: '#4527A0',
          from: 'Joker Won',
          message: 'Good night.'
        },
        {
          id: 4,
          time: '3:12pm',
          color: '#FF5722',
          from: 'JokerWon',
          message: 'Love playing basketball.'
        },
        {
          id: 3,
          time: '10:32am',
          color: '#69F0AE',
          from: 'Joker Won',
          message: 'Studying...'
        },
        {
          id: 2,
          time: '9:27am',
          color: '#FFAB00',
          from: 'Charles Xie',
          message: 'How a nice morning!'
        },
        {
          id: 1,
          time: '8:15am',
          color: '#FFEA00',
          from: 'Joker Won',
          message: 'Good morning! ^_^'
        },
      ]
    }
  },
  components: {
  }
}
</script>
