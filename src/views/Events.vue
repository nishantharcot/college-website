<template>
  <div>
    <v-row id="screen1" app>
      <v-col id="screen1-content" cols="12" sm="12">
        <h1 class="display-1 centerClass">Gallery</h1>
      </v-col>
    </v-row>
    <v-row class="screen2">
      <v-col cols="1"></v-col>
      <v-col cols="12" sm="12" md="5">
        <h3 class="mb-5 ml-5">Photo gallery</h3>
        <p class="ml-5">
          Even though all of the programs provided by LIGS University are 100%
          online and the students don't have to visit the campus of the
          university in Hawaii, our campus in Prague, Czech Republic often
          organizes events such as the annual LIGS AWARDS. We would like to
          share a few photos from these wonderful events with you.
        </p>
        <v-btn color="info" class="ml-5 mx-auto" rounded>View All</v-btn>
      </v-col>
      <v-col cols="12" sm="12" md="5">
        <v-img src="../assets/gallery-1.jpg"></v-img>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row class="screen2">
      <v-col cols="1"></v-col>
      <v-col cols="12" sm="12" md="5">
        <h3 class="mb-5 ml-5">Video gallery</h3>
        <p class="ml-5">
          This section contains various videos that help introduce LIGS
          University. We hope you enjoy watching!
        </p>
        <v-btn color="info" class="ml-5 mx-auto" rounded>View All</v-btn>
      </v-col>
      <v-col cols="12" sm="12" md="5">
        <!-- <iframe
          :width="width"
          :height="height"
          src="https://www.youtube.com/embed/tgbNymZ7vqY"
        ></iframe>-->

        <a href="https://www.youtube.com/watch?v=qW0uzPJEO10">
          <v-img src="../assets/contact-1.jpg"></v-img>
        </a>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    width: 450,
    height: 300
  })
};
</script>

<style lang="scss" scoped>
.centerClass {
  text-align: center;
}
#screen1 {
  min-height: 40vh;
  display: flex;
  justify-content: center;
  align-items: center;
  // background-color: yellow;
}

#screen1-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.screen2 {
  min-height: 75vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
