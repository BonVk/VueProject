<template>
  <v-app dark>
    <div v-if="announce" class="announce">
      <v-container>
        <v-row class="d-inline-flex align-center justify-space-between"> 
        <span>Join us at Config live in SF. Attend Config June 21-22 in person and get access to IRL-only Figma workshops, networking, and community. </span>
        <v-btn icon @click="closeAnnounce">
        <v-icon>mdi-close</v-icon>
      </v-btn>
       </v-row>
      </v-container>
    </div>

    <v-main>
      <v-row class="d-flex justify-space-between" style="padding: 0px 30px; margin-top: 30px;">
       <a href="/"><FigmaLogo /></a> 
      
      <div>
        <a href="/pricing">Pricing</a> 
      </div>
    </v-row>
    
        <Nuxt />      

    </v-main>
 
    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import FigmaLogo from '../components/FigmaLogo.vue';

export default {
    name: "DefaultLayout",
    data() {
        return {
            announce: true,
            items: [
                {
                    icon: "mdi-apps",
                    title: "Welcome",
                    to: "/"
                },
                {
                    icon: "mdi-chart-bubble",
                    title: "Inspire",
                    to: "/inspire"
                }
            ],
            title: "Vuetify.js"
        };
    },
    methods: {
        closeAnnounce() {
            this.announce = false;
        }
    },
    components: { FigmaLogo }
}
</script>
<style>
.announce {
  background-color: rgb(252, 221, 236);
}
</style>
