<template>
  <div>
    <v-row id="screen1" app>
      <v-col id="screen1-content" cols="12" sm="12">
        <h1 id="mainHeading" class="display-1 centerClass">DEGREES</h1>
        <h5 id="secondHeading" class="centerClass mt-10">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit phasellus
          trist.
        </h5>
      </v-col>
    </v-row>
    <v-row class="screen2">
      <v-col cols="1"></v-col>
      <v-col cols="12" sm="12" md="5">
        <v-img src="../assets/degree-1.jpg"></v-img>
      </v-col>
      <v-col cols="12" sm="12" md="5">
        <v-btn class="mb-5 ml-5" color="warning">$21,500</v-btn>
        <h3 class="mb-5 ml-5">COMPUTER SCIENCE</h3>
        <p class="ml-5">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eu
          mauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse eget
          ante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis
          lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunc
          lectus ut dui.
        </p>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row class="screen2">
      <v-col class="order-1" cols="1"></v-col>
      <v-col class="order-3" cols="12" sm="12" md="5">
        <v-btn class="mb-5 ml-5" color="warning">$11,300</v-btn>
        <h3 class="mb-5 ml-5">LIBERAL ARTS</h3>
        <p class="ml-5">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eu
          mauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse eget
          ante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis
          lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunc
          lectus utd.
        </p>
      </v-col>
      <v-col
        v-if="$vuetify.breakpoint.mdAndUp"
        class="order-3"
        cols="12"
        sm="12"
        md="5"
      >
        <v-img src="../assets/degree-2.jpg"></v-img>
      </v-col>
      <v-col v-else class="order-2" cols="12" sm="12" md="5">
        <v-img src="../assets/degree-2.jpg"></v-img>
      </v-col>
      <v-col class="order-4" cols="1"></v-col>
    </v-row>
    <v-row class="screen2">
      <v-col cols="1"></v-col>
      <v-col cols="12" sm="12" md="5">
        <v-img src="../assets/degree-3.jpg"></v-img>
      </v-col>
      <v-col cols="12" sm="12" md="5">
        <v-btn class="mb-5 ml-5" color="warning">$21,900</v-btn>
        <h3 class="mb-5 ml-5">HUMANITIES</h3>
        <p class="ml-5">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eu
          mauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse eget
          ante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis
          lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunc
          lectus ut dui.
        </p>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row class="screen2">
      <v-col class="order-1" cols="1"></v-col>
      <v-col class="order-3" cols="12" sm="12" md="5">
        <v-btn class="mb-5 ml-5" color="warning">$34,000</v-btn>
        <h3 class="mb-5 ml-5">APPLIED SCIENCE</h3>
        <p class="ml-5">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eu
          mauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse eget
          ante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis
          lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunc
          lectus utd.
        </p>
      </v-col>
      <v-col
        v-if="$vuetify.breakpoint.mdAndUp"
        class="order-3"
        cols="12"
        sm="12"
        md="5"
      >
        <v-img src="../assets/degree-4.jpg"></v-img>
      </v-col>
      <v-col v-else class="order-2" cols="12" sm="12" md="5">
        <v-img src="../assets/degree-4.jpg"></v-img>
      </v-col>
      <v-col class="order-4" cols="1"></v-col>
    </v-row>
    <v-row id="screen4" class="theme--dark">
      <v-col cols="1"></v-col>
      <v-col
        cols="12"
        md="2"
        sm="12"
        v-for="item in collegeStatistics"
        :key="item.title"
      >
        <div class="screen4Card">
          <h2 class="centerClass">{{ item.title }}</h2>
          <hr
            role="separator"
            aria-orientation="horizontal"
            class="v-divider lineAdjust"
          />
          <h4 class="centerClass">{{ item.label }}</h4>
        </div>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row id="screen3" app>
      <v-col cols="1"></v-col>
      <v-col class="centerClass" cols="10">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus eu
          mauris eleifend, rhoncus metus vel, vestibulum odio. Suspendisse eget
          ante vel arcu pretium eleifend vel quis dolor. In aliquam, elit quis
          lacinia ornare, nunc mauris aliquam erat, scelerisque laoreet nunc
          lectus utd.
        </p>
        <v-btn x-large color="warning" class="mt-5">
          <v-icon class="mr-3">fas fa-graduation-cap</v-icon>ENROLL TODAY
        </v-btn>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    collegeStatistics: [
      {
        title: 19228,
        label: "Success Stories"
      },
      {
        title: 9213,
        label: "Courses"
      },
      {
        title: 1742,
        label: "Happy Students"
      },
      {
        title: 67,
        label: "Years Experience"
      }
    ]
  })
};
</script>

<style lang="scss" scoped>
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Roboto Slab", serif !important;
}
#screen1 {
  min-height: 50vh;
  display: flex;
  justify-content: center;
  align-items: center;
  // background-color: yellow;
  background-image: url("../assets/gallery.jpg");
  background-size: cover;
  background-position: center;
  color: white;
}

#mainHeading {
  font-weight: 900 !important;
}

#secondHeading {
  font-weight: 600;
}

#screen1-content {
  min-height: 50vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: rgba(black, 0.7);
  z-index: 2;
}
hr {
  width: 20%;
  margin: 0 auto;
  border-top: 5px solid aqua;
}

.screen2 {
  min-height: 65vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

#screen4 {
  // height: 40vh;
  min-height: 40vh;
  display: flex;
  justify-content: space-around;
  align-content: space-around;
  background-color: #1a237e;
  color: white;
}

.screen4Card {
  display: flex;
  height: 15vh;
  flex-direction: column;
  justify-content: space-between;
}

#screen3 {
  min-height: 30vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.centerClass {
  text-align: center;
}
</style>
