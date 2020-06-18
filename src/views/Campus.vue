<template>
  <div>
    <v-row id="screen1" app>
      <v-col id="screen1-content" cols="12" sm="12">
        <h1 class="display-1 centerClass mb-5">CAMPUS LIFE</h1>
        <ol class="ml-5">
          <li>What are three things you are looking forward to in college?</li>
          <li>What makes you want to go to college?</li>
          <li>What are some differences between high school and college?</li>
        </ol>
      </v-col>
    </v-row>
    <v-row class="screen2">
      <v-col class="order-1" cols="1"></v-col>
      <v-col class="order-3" cols="12" sm="12" md="5">
        <h3 class="mb-5 ml-5">WHY GO TO OUR SCHOOL</h3>
        <p class="ml-5">
          You will probably have less contact with your professors. The workload
          and expectations are different as well. You may have weekly reading
          assignments but have fewer, larger projects to turn in for the
          semester. Your grade may be based on only two tests for the whole
          semester — meaning it is important to plan your study schedule and how
          you use your time.
        </p>
        <div class="ml-5" v-for="item in screen2Data" :key="item.label">
          <div class="screen2Icons">
            <v-icon>{{ item.icon }}</v-icon>
            <p class="mt-4 ml-3">{{ item.label }}</p>
          </div>
        </div>
      </v-col>
      <v-col
        v-if="$vuetify.breakpoint.mdAndUp"
        class="order-3"
        cols="12"
        sm="12"
        md="5"
      >
        <a href="https://www.youtube.com/watch?v=qW0uzPJEO10" target="_blank">
          <v-img src="../assets/videoImage2.jpg"></v-img>
        </a>
      </v-col>
      <v-col v-else class="order-2" cols="12" sm="12" md="5">
        <a href="https://www.youtube.com/watch?v=qW0uzPJEO10" target="_blank">
          <v-img src="../assets/videoImage2.jpg"></v-img>
        </a>
      </v-col>
      <v-col class="order-4" cols="1"></v-col>
    </v-row>
    <v-row class="screen2">
      <v-col cols="1"></v-col>
      <v-col cols="12" sm="12" md="5">
        <a href="https://www.youtube.com/watch?v=qW0uzPJEO10" target="_blank">
          <v-img src="../assets/campus2.jpg"></v-img>
        </a>
      </v-col>
      <v-col cols="12" sm="12" md="5">
        <h3 class="mb-5 ml-5">LIVE STREAM</h3>
        <p class="ml-5">
          Equally important to differences in academics are the increased
          opportunities to have a social life, especially if you live in a
          dormitory. Your dorm or campus may offer weekend activities or you may
          be invited to go out during the week. You will have to decide when to
          do laundry, what time to get up for class, when to eat and if you want
          to participate in a student organization.
        </p>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row class="screen3">
      <v-col cols="1"></v-col>
      <v-col cols="12" md="10">
        <h2 class="ml-5">STUDENT VIDEOS</h2>
        <p class="mt-5 ml-5">
          One of the biggest changes in college is that you have much more
          freedom (for example to set your schedule, choose your major and go to
          class)
        </p>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row class="screen4">
      <v-col cols="1"></v-col>
      <v-col class="mx-auto" cols="12" md="3">
        <a href="https://www.youtube.com/watch?v=qW0uzPJEO10" target="_blank">
          <v-img src="../assets/videoImage1.jpg"></v-img>
        </a>
      </v-col>
      <v-col class="mx-auto" cols="12" md="3">
        <a href="https://www.youtube.com/watch?v=qW0uzPJEO10" target="_blank">
          <v-img src="../assets/videoImage2.jpg"></v-img>
        </a>
      </v-col>
      <v-col class="mx-auto" cols="12" md="3">
        <a href="https://www.youtube.com/watch?v=qW0uzPJEO10" target="_blank">
          <v-img src="../assets/videoImage3.jpg"></v-img>
        </a>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row id="screen5">
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
          <h4 class="centerClass">{{ item.label }}</h4>
        </div>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row class="screen3">
      <v-col cols="1"></v-col>
      <v-col cols="12" md="10">
        <h2 class="ml-5">EVENTS</h2>
        <p class="mt-5 ml-5">
          HNC, HND, Undergraduate and Postgraduate Recruitment day 2020 (
          National & International)
        </p>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row class="screen4">
      <v-col cols="1"></v-col>
      <v-col class="mx-auto eventCard" cols="12" md="3">
        <!-- <v-img src="../assets/event-1.jpg"></v-img> -->
        <v-card class="mx-auto" max-width="400">
          <v-img
            class="white--text align-end"
            height="200px"
            src="../assets/event-1.jpg"
          ></v-img>

          <v-card-subtitle class="pb-0"
            >Recruitment Day Philippines 2020</v-card-subtitle
          >

          <v-card-text class="text--primary">
            <div>June 01 at 09:00 am</div>
            <div>Recruitment day – Manila, Philippines</div>
          </v-card-text>

          <v-card-actions>
            <v-btn color="orange" text>Share</v-btn>

            <v-btn color="orange" text>Explore</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col class="mx-auto eventCard" cols="12" md="3">
        <!-- <v-img src="../assets/event-1.jpg"></v-img> -->
        <v-card class="mx-auto" max-width="400">
          <v-img
            class="white--text align-end"
            height="200px"
            src="../assets/event-2.jpg"
          ></v-img>

          <v-card-subtitle class="pb-0"
            >Recruitment Day - London, United Kingdom</v-card-subtitle
          >

          <v-card-text class="text--primary">
            <div>July 03 at 09:00 am</div>
            <div>16 London St, Paddington, London, United Kingdom</div>
          </v-card-text>

          <v-card-actions>
            <v-btn color="orange" text>Share</v-btn>

            <v-btn color="orange" text>Explore</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col class="mx-auto eventCard" cols="12" md="3">
        <!-- <v-img src="../assets/event-1.jpg"></v-img> -->
        <v-card class="mx-auto" max-width="400">
          <v-img
            class="white--text align-end"
            height="200px"
            src="../assets/event-3.jpg"
          ></v-img>

          <v-card-subtitle class="pb-0"
            >Recruitment Day - Health And Social Care</v-card-subtitle
          >

          <v-card-text class="text--primary">
            <div>June 01 at 09:00 am</div>
            <div>Leicester Business Centre, Leiecster, United Kingdom</div>
          </v-card-text>

          <v-card-actions>
            <v-btn color="orange" text>Share</v-btn>

            <v-btn color="orange" text>Explore</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row id="last-screen">
      <v-col cols="1"></v-col>
      <v-col class="flexClass" cols="12" md="10">
        <h1 class="mx-auto centerClass">YOUR FUTURE STARTS HERE.</h1>
        <h3 class="mx-auto centerClass">Health and Social Care Courses</h3>
        <p>
          Browse through our available courses in health and social care to find
          the perfect course to progress you career. We offer Cache
          qualifications in health and social care which can be studied online
          through our virtual campus with expert support throughout your
          enrolment.
        </p>
        <v-btn x-large color="info">
          <v-icon>fas fa-graduation-cap</v-icon>ENROLL TODAY
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
    ],
    screen2Data: [
      {
        icon: "fas fa-graduation-cap",
        label: "Integrity"
      },
      {
        icon: "fas fa-users",
        label: "Diversity"
      },
      {
        icon: "fas fa-trophy",
        label: "Excellence"
      },
      {
        icon: "far fa-dot-circle",
        label: "Collaboration"
      }
    ]
  })
};
</script>

<style lang="scss" scoped>
.centerClass {
  text-align: center;
}
.last-screen-arrange {
  display: flex;
  justify-content: space-between;
}
.flexClass {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.screen4Card {
  display: flex;
  height: 15vh;
  flex-direction: column;
  justify-content: space-between;
}

.screen2Icons {
  display: flex;
}

.eventCard {
  min-height: 70vh !important;
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

.screen3 {
  min-height: 30vh;
  display: flex;
  align-items: center;
}

#screen3-videos {
  display: flex;
}

.screen4 {
  min-height: 50vh;
}

#screen5 {
  // height: 40vh;
  min-height: 40vh;
  display: flex;
  justify-content: space-around;
  align-content: space-around;
  // background-color: pink;
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
</style>
