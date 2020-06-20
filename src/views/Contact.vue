<template>
  <div>
    <StartScreen pageHeading="CONTACT US" />
    <v-row class="screen2">
      <v-col cols="1"></v-col>
      <v-col cols="12" sm="12" md="5">
        <h3 class="mb-10">WELCOME!</h3>
        <h2 class="mb-5">Welcome to London College of Technology</h2>
        <p>
          London College Of Technology is an education institute situated in the
          hearts of London, we thrive our focus on providing excellence career
          developments and continuing education. We are committed to enriching
          the lives at all students and delivering a wide range of high quality
          learning experiences.
        </p>
        <p>
          On successful attainment students may gain access to Bachelors and
          Master programs offered at our partnership colleges and Universities.
        </p>
        <v-btn color="warning">
          Read More
          <v-icon class="ml-3">fas fa-arrow-right</v-icon>
        </v-btn>
      </v-col>
      <v-col cols="12" sm="12" md="5">
        <v-img src="../assets/contact-1.jpg"></v-img>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row id="last-screen">
      <v-col cols="1"></v-col>
      <v-col class="flexClass" cols="12" md="10">
        <h1 class="mx-auto centerClass">ENROLL FAST</h1>
        <p>Admission for Fall 2021 classes closes on Aug. 1!</p>
        <v-btn x-large color="warning">
          <v-icon>fas fa-graduation-cap</v-icon>ENROLL TODAY
        </v-btn>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
  </div>
</template>

<script>
import StartScreen from "@/components/StartScreen.vue";
export default {
  components: {
    StartScreen
  }
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
.centerClass {
  text-align: center;
}
.flexClass {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
#screen1 {
  background-image: url("../assets/contact.jpg");
}

#last-screen {
  min-height: 50vh;
}

#last-screen-left {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  max-width: 40vw;
}

.screen2 {
  min-height: 70vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
