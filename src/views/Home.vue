<template>
  <div class="home pb-0">
    <v-row id="screen1" app>
      <v-col id="screen1-content" cols="12" sm="12">
        <h1 id="mainHeading" class="display-1 centerClass">
          HOW WILL YOU FORGE YOUR FUTURE?
        </h1>
        <v-btn x-large color="warning" class="mt-5">
          <v-icon class="mr-3">fas fa-graduation-cap</v-icon>ENROLL TODAY
        </v-btn>
      </v-col>
    </v-row>
    <v-row id="screen2" app>
      <v-col class="flexClass" cols="12" sm="12">
        <h1 class="display-1">ABOUT US</h1>
        <p class="mt-10 centerClass">
          Here you will find guidelines about how to use the portal to study at
          LCT
        </p>
      </v-col>
    </v-row>
    <v-row id="screen3">
      <v-col class="order-1" cols="1"></v-col>
      <v-col class="order-3" cols="12" sm="12" md="5">
        <h3 class="mb-5">Welcome to London College of Technology</h3>
        <p>
          London College Of Technology is an education institute situated in the
          hearts of London, we thrive our focus on providing excellence career
          developments and continuing education. We are committed to enriching
          the lives at all students and delivering a wide range of high quality
          learning experiences.
        </p>
        <p>
          Studying at LCT will provide you with the tools you need to forge a
          bright future for yourself. With experience in helping students
          achieve their potential, we are committed to excellence in learning
          and teaching.
        </p>
        <p>
          London college of Technology organise yearly national and
          international media and fine arts competitions. These competitions
          will improve the students’ confidence and encourage them to succeed.
        </p>
        <p>
          On successful attainment students may gain access to Bachelors and
          Master programs offered at our partnership colleges and Universities.
        </p>
      </v-col>
      <v-col
        v-if="$vuetify.breakpoint.mdAndUp"
        class="order-3"
        cols="12"
        sm="12"
        md="5"
      >
        <div>
          <v-img src="../assets/about-us2.jpg"></v-img>
        </div>
      </v-col>
      <v-col class="order-2" cols="12" sm="12" md="5" v-else>
        <div>
          <v-img src="../assets/about-us2.jpg"></v-img>
        </div>
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
    <v-row class="mt-10" id="screen5">
      <v-col cols="2"></v-col>
      <v-col class="flexClass" cols="8">
        <h1 class="display-1">WHAT'S HAPPENING</h1>
        <p class="mt-10">
          London College of Technology Studies is a privately funded FE college
          offering a broad range of vocational, professional and academic
          programmes. Our teachers are experienced, appropriately qualified and
          highly motivated. Our teachers use all the very latest equipment to
          deliver our courses and keep up to date with all the latest techniques
          in teaching.
        </p>
      </v-col>
      <v-col cols="2"></v-col>
    </v-row>
    <v-row id="screen6" class="mt-0">
      <v-col class="flexClass" cols="12" sm="12">
        <h1 class="display-1 centerClass white--text">
          YOUR FUTURE STARTS HERE.
        </h1>
        <v-btn large class="mt-5" color="warning">
          LEARN MORE
          <v-icon class="ml-2">mdi mdi-open-in-new</v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </div>
</template>

<style lang="scss" scoped>
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Roboto Slab", serif !important;
}
.flexClass {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
hr {
  width: 20%;
  margin: 0 auto;
  border-top: 5px solid aqua;
}
#mainHeading {
  font-weight: 900 !important;
}
#screen1 {
  min-height: 90vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url("../assets/home-hero.jpg");
  background-size: cover;
  background-position: center;
  color: white;
}
#screen1-content {
  min-height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: rgba(black, 0.7);
  z-index: 2;
  // color: darkblue;
}

#screen2 {
  min-height: 40vh;
  // height: 40vh;
  // background-color: aqua;
}

#screen3 {
  min-height: 80vh;
  // height: 80vh;
  // background-color: aqua;
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

// #screen5 {
//   // height: 50vh;
// }

#screen6 {
  height: 40vh;
  background-color: #536dfe;
}

.centerClass {
  text-align: center;
}
</style>

<script>
// @ is an alias to /src

export default {
  name: "Home",
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
