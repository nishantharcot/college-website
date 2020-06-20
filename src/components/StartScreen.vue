<template>
  <v-row id="screen1" app>
    <v-col id="screen1-content" cols="12" sm="12">
      <h1 id="mainHeading" class="display-1 centerClass">
        {{ pageHeading }}
      </h1>
      <div v-if="Boolean(caption) === true">
        <h5 id="secondHeading" class="centerClass mt-10">
          {{ caption }}
        </h5>
      </div>
      <div v-if="Boolean(extraPoints) === true">
        <ol id="secondHeading" class="ml-5 mt-5">
          <li>What are three things you are looking forward to in college?</li>
          <li>What makes you want to go to college?</li>
          <li>What are some differences between high school and college?</li>
        </ol>
      </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  props: {
    pageHeading: {
      type: String,
      required: true
    },
    caption: {
      type: String
    },
    extraPoints: {
      type: Array[String]
    }
  }
};
</script>

<style lang="scss" scoped>
#screen1 {
  min-height: 50vh;
  display: flex;
  justify-content: center;
  align-items: center;
  // background-color: yellow;
  background-size: cover;
  background-position: center;
  color: white;
}

.centerClass {
  text-align: center;
}

#mainHeading {
  font-weight: 900 !important;
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

#secondHeading {
  font-weight: 600;
}
</style>
