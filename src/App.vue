<template>
  <v-app id="inspire">
    <v-app-bar app>
      <!-- <v-img src="./assets/collegeLogo.png"></v-img> -->
      <v-toolbar-title id="mainHeading" class="display-1"
        >Becton College</v-toolbar-title
      >
      <v-spacer></v-spacer>
      <div v-if="$vuetify.breakpoint.smAndDown">
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      </div>
      <div v-else>
        <v-btn v-for="link in links" :key="link.label" :to="link.url" text>{{
          link.label
        }}</v-btn>
      </div>
    </v-app-bar>

    <v-navigation-drawer
      v-if="$vuetify.breakpoint.smAndDown"
      v-model="drawer"
      app
      right
    >
      <v-list dense>
        <v-list-item v-for="link in links" :key="link.label" :to="link.url">
          <v-list-item-content>
            <v-list-item-title>{{ link.label }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container fluid class="containerStyle pt-0 pb-0">
        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer padless>
      <v-container class="pt-0">
        <v-row>
          <v-col class="pl-2" cols="12" md="3" xs="12">
            <v-main class="pa-1 mr-3" outlined tile>
              <h3 class="display pl-2">Becton College</h3>
              <v-col v-for="item in footerStart" :key="item.text">
                <v-icon class="mr-2">{{ item.icon }}</v-icon>
                &nbsp;
                {{ item.text }}
              </v-col>
            </v-main>
          </v-col>
          <v-col
            cols="12"
            md="2"
            xs="12"
            v-for="item in footerResources"
            :key="item.heading"
          >
            <div class="pa-2" outlined tile>
              <h3 class="display pl-2">{{ item.heading }}</h3>
              <v-col v-for="data in item.data" :key="data">{{ data }}</v-col>
            </div>
          </v-col>
          <v-col class="mt-1" cols="12" md="3" xs="12">
            <v-main class="pa-1 mr-3" outlined tile>
              <h3 class="display pl-2">WEEKLY NEWSLETTER</h3>
              <v-text-field label="Name" type="text"></v-text-field>
              <v-text-field label="Email" type="enail"></v-text-field>
              <v-btn x-large block color="warning">Subscribe</v-btn>
            </v-main>
          </v-col>
        </v-row>
      </v-container>
      <v-card color="grey darken-3" class="flex" flat tile>
        <v-card-title>
          <strong class="subheading footer">&copy; All rights reserved</strong>

          <v-spacer></v-spacer>

          <v-btn v-for="icon in icons" :key="icon" class="mx-4" icon>
            <v-icon color="white" class="footer" size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-title>
      </v-card>
    </v-footer>
  </v-app>
</template>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Quicksand&display=swap");
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Roboto Slab", serif !important;
}

*:not(.v-icon) {
  font-family: "Quicksand", sans-serif;
}
.footer {
  color: white;
}
.white {
  color: white;
}
.containerStyle {
  padding: -12px !important;
}
#mainHeading {
  font-weight: 900 !important;
}
</style>
<script>
export default {
  name: "LayoutsDemosBaselineFlipped",
  props: {
    source: String
  },
  data: () => ({
    drawer: null,
    footerStart: [
      {
        icon: "fas fa-phone",
        text: "01902275538"
      },
      {
        icon: "fas fa-envelope",
        text: "info@becton.co.uk"
      },
      {
        icon: "fas fa-map-marker-alt",
        text:
          "West Midlands House Gipsy Lane, Willenhall West Midlands, WV13 2HA ,United Kingdom"
      }
    ],
    footerResources: [
      {
        heading: "FEATURES",
        data: ["Pricing", "Education", "Refer a Friend", "Updates", "Beta"]
      },
      {
        heading: "COMPANY",
        data: ["Design", "Prototype", "Colloborate", "Sketch", "Photoshop"]
      },
      {
        heading: "GET STARTED",
        data: ["Tutorials", "Resources", "Guides", "Example", "Docs"]
      }
    ],
    icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
    links: [
      {
        label: "Home",
        url: "/"
      },
      {
        label: "About",
        url: "/about"
      },
      {
        label: "Campus",
        url: "/campus"
      },
      {
        label: "Degree",
        url: "/degree"
      },
      {
        label: "Programs",
        url: "/programs"
      },
      {
        label: "Events",
        url: "/events"
      },
      {
        label: "Contact",
        url: "/contact"
      }
    ]
  })
};
</script>
