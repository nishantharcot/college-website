<template>
  <div class="about">
    <v-row id="screen1" app>
      <v-col id="screen1-content" cols="12" sm="12">
        <h1 class="display-1 centerClass">ABOUT US</h1>
      </v-col>
    </v-row>
    <v-row id="screen2">
      <v-col cols="1"></v-col>
      <v-col cols="12" md="10">
        <v-card color="basil">
          <!-- <v-card-title class="text-center justify-center py-6">
            <h1 class="font-weight-bold display-3 basil--text">BASiL</h1>
          </v-card-title>-->
          <v-tabs
            v-model="tab"
            background-color="transparent"
            color="basil"
            grow
          >
            <v-tab v-for="item in items" :key="item">{{ item }}</v-tab>
          </v-tabs>

          <v-tabs-items v-model="tab">
            <v-tab-item v-for="item in items" :key="item">
              <v-card color="basil" flat>
                <v-card-text v-if="item === 'ABOUT LCT'">
                  <div class="about-content">
                    <h2>About</h2>
                    <p>
                      Our vision is to promote educational opportunity and
                      social justice by providing high-quality education and
                      trainings to all who wish to realise their ambitions and
                      fulfil their potential.
                    </p>
                    <p>
                      We are committed to promoting equal opportunities for all
                      and we monitor ourselves to make sure we live up to our
                      ideals.
                    </p>
                    <p>
                      London College of Technology is a Community employment and
                      training support providers.
                    </p>
                    <p>
                      We are committed to enriching the lives of all members of
                      the community and to creating new opportunities for them.
                      We have links to a range of community based services and
                      we are experienced at introducing the people we support to
                      a full range of community programmes.
                    </p>
                    <p>
                      The institution caters for all walks of life i.e. from
                      refugees, unemployed and professional of all ages, gender,
                      race and colour. We implement an excellent equal
                      opportunity policy and cater for the social and cultural
                      needs of the local and international population.
                    </p>
                  </div>
                </v-card-text>
                <v-card-text v-if="item === 'WHY LCT'">
                  <div class="about-content">
                    <h2 class="mb-5">
                      Why choose London College of Technology?
                    </h2>
                    <h3 class="mb-3">
                      The College’s mission is to be open to people, places,
                      methods and ideas.
                    </h3>
                    <p>
                      Nearly all of our courses have no formal entry
                      requirements, either prior qualifications or experience.
                      We allow people who have missed out on education to fulfil
                      their potential and achieve qualification that will see
                      them succeed forward in their career
                    </p>
                    <p>
                      We believe that it is the qualifications and practical
                      experience with which our students leave, rather than
                      those with which they enter, that count.
                    </p>
                    <p>
                      We have students of all ages and backgrounds including
                      overseas: school leavers who choose to begin their careers
                      while they study, people wanting to develop or update
                      their skills, or change career entirely, and retired
                      people wanting to explore new interests and keep mentally
                      active.
                    </p>
                    <p>
                      Learners at London College of Technology have at least one
                      thing in common: they are all learning for success. The
                      College is committed to promoting equality and valuing
                      diversity, as we have students of all ages, backgrounds
                      and beliefs.
                    </p>
                    <p>
                      In our College there will be opportunities to make new
                      friends, take part in national competitions, gain work
                      experience, be involved with work experience and visit new
                      and exciting places, amongst other activities, ensuring
                      your time here is enjoyable and rewarding.
                    </p>
                  </div>
                </v-card-text>
                <v-card-text v-if="item === 'LIFE AT LCT'">
                  <div class="about-content">
                    <h2 class="mb-5">Life at London college of technology</h2>
                    <p>
                      London College of Technology provides a warm and vibrant
                      environment for students from all walks of life. The
                      student will find the learning experience relaxed and
                      enjoyable and that it will stimulate and stretch mental
                      ability. Leicester is an exciting and diverse city with
                      its many shopping areas including the High cross and
                      Haymarket shopping centres, Leicester has something for
                      all tastes.
                    </p>
                    <p>
                      There is a vast choice of bars and restaurants to enjoy
                      and plenty of entertainment available at the various
                      cinemas and theatres around the city. Because the city has
                      such a diverse culture it hosts events such as the
                      Caribbean Carnival, Diwali lights and the Summer Sundae
                      music festival. It is also home to the National Space
                      Centre.
                    </p>
                    <p>
                      Known officially as the The Golden Mile comprising
                      Belgrave Road and Melton Road, it is home to the largest
                      selection of Indian jewellery shops outside of India. If
                      you’re looking for true Indian restaurants, sweetmarts and
                      shops which sell items from the Indian culture this is the
                      place to be.
                    </p>
                    <p>
                      The classrooms at LCT are modern, spacious, well lit and
                      impressive with all the latest technology. You’ll feel
                      warmth with our staff and tutors, who are all friendly and
                      welcoming.
                    </p>
                    <p>
                      London College of Technology makes sure that all students
                      feel at home in the multi-cultural and multi-lingual
                      atmosphere provided by the College.
                    </p>
                    <p>
                      We look forward to welcoming you and helping you to
                      achieve your learning objectives.
                    </p>
                  </div>
                </v-card-text>
              </v-card>
            </v-tab-item>
          </v-tabs-items>
        </v-card>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
    <v-row id="screen3" app>
      <h2>YOUR FUTURE STARTS HERE.</h2>
      <v-btn color="info">LEARN MORE</v-btn>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    tab: null,
    items: ["ABOUT LCT", "WHY LCT", "LIFE AT LCT"],
    text:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
  })
};
</script>

<style lang="scss" scoped>
.basil {
  background-color: #fffbe6 !important;
}
.basil--text {
  color: #356859 !important;
}
.about-content {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  min-height: 70vh;
}
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

#screen2 {
  min-height: 100vh;
}

#screen3 {
  min-height: 30vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
