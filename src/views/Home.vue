
  <template>
  <div><hello-world></hello-world>


  <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-img
      src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
      height="200px"
    ></v-img>

    <v-card-title>
      06- Components :To do
    </v-card-title>

    

    <v-card-actions>
      <v-btn
        color="orange lighten-2"
        text
      >
        More info
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          Todo is in TODO menu.
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>

  </div>
</template>


<script>

import HelloWorld from "../components/HelloWorld.vue";


export default {
  data: () => ({
      show: false,
    }),
  name: "Home",

  components: {
    HelloWorld,

  },
};
</script>
