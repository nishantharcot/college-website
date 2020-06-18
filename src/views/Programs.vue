<template>
  <div>
    <v-row>
      <v-col cols="1"></v-col>
      <v-col cols="10">
        <h1 id="programHeading" class="display basil--text">OUR COURSES</h1>
        <v-expansion-panels>
          <v-expansion-panel v-for="course in courses" :key="course.title">
            <v-expansion-panel-header>{{
              course.title
            }}</v-expansion-panel-header>
            <v-expansion-panel-content>
              <div v-if="$vuetify.breakpoint.smAndDown">
                <h3 class="display mb-3">Overview</h3>
                <p>{{ course.overview }}</p>
              </div>
              <div v-if="$vuetify.breakpoint.mdAndUp">
                <Program :course="course" />
              </div>
              <div v-if="$vuetify.breakpoint.smAndDown">
                <v-btn color="success">Learn More</v-btn>
              </div>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
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
import Program from "./Program.vue";
export default {
  data: () => ({
    courses: [
      {
        title: "OTHM LEVEL 3 CERTIFICATE IN BUSINESS STUDIES",
        overview:
          "The objective of Level 3 Certificate in Business Studies qualification is to provide learners with an in depth understanding of the operations and structure of businesses. Successful completion of this qualification will equip learners with some of the underpinning knowledge and skills required to succeed in employment or further studies."
      },
      {
        title: "OTHM LEVEL 3 DIPLOMA IN BUSINESS STUDIES",
        overview:
          "The objective of Level 3 Diploma  in Business Studies qualification is to provide learners with an in depth understanding of the operations and structure of businesses. Successful completion of this qualification will equip learners with some of the underpinning knowledge and skills required to succeed in employment or further studies."
      },
      {
        title: "OTHM LEVEL 4 DIPLOMA IN BUSINESS MANAGEMENT",
        overview:
          "The objective of  Level 4 Diploma in Business Management qualification is to provide learners with an excellent foundation for building a career in a range of organisations. It designed to ensure each learner is ‘business ready’: a confident, independent thinker with a detailed knowledge of business and management and equipped with the skills to adapt rapidly to change."
      },
      {
        title: "OTHM LEVEL 6 DIPLOMA IN BUSINESS MANAGEMENT",
        overview:
          "The objective of the OTHM Level 6 Diploma in Business Management qualification is to provide learners with an excellent foundation for a career in a range of organisations. It designed to ensure that each learner is ‘business ready’: a confident, independent thinker with a detailed knowledge of business and management and equipped with the skills to adapt rapidly to change. The content of the qualification is focused on leadership and people management, strategic human resource management, operations management, sustainable business practice, financial decision making as well as the business research skills expected of a manager. The qualification is ideal for those who have started, or are planning to move into, a career in private or public sector business. Successful completion of the Level 6 Diploma in Business Management qualification will provide learners with the opportunity to progress to further study or employment."
      },
      {
        title: "QUALIFI LEVEL 3 DIPLOMA IN BUSINESS MANAGEMENT",
        overview:
          "This suite of Qualifications provides a realistic and broad opportunity for Learners seeking career and professional development. They will support Learners in realising their potential and by association the prospects of the organisations they work with or for. The Qualification provides a rich mix of disciplines and skills development opportunities. Learners will gain insight into the functioning, objectives and processes of organisations, appreciating their diversity and the influences and impact of external forces on them."
      },
      {
        title: "QUALIFI LEVEL 4 CERTIFICATE IN BUSINESS MANAGEMENT",
        overview:
          "This suite of Qualifications provides a realistic and broad opportunity for Learners seeking career and professional development. They will support Learners in realising their potential and by association the prospects of the organisations they work with or for. Management of a range of business operations and functions, the management of specific challenges for organisations will introduce Learners to management theory, practice and models that will provide valuable knowledge and know-how."
      },
      {
        title: "QUALIFI LEVEL 5 DIPLOMA IN BUSINESS ENTERPRISE",
        overview:
          "This suite of Qualifications provides a realistic and broad opportunity for Learners seeking career and professional development. They will support Learners in realising their potential and by association the prospects of the organisations they work with or for. Management of a range of business operations and functions, the management of specific challenges for organisations will introduce Learners to management theory, practice and models that will provide valuable knowledge and know-how."
      },
      {
        title: "QUALIFI LEVEL 5 DIPLOMA IN BUSINESS MANAGEMENT",
        overview:
          "This suite of Qualifications provides a realistic and broad opportunity for Learners seeking career and professional development. They will support Learners in realising their potential and by association the prospects of the organisations they work with or for. Management of a range of business operations and functions, the management of specific challenges for organisations will introduce Learners to management theory, practice and models that will provide valuable knowledge and know-how."
      },
      {
        title: "QUALIFI LEVEL 6 DIPLOMA IN BUSINESS ADMINISTRATION",
        overview:
          "This suite of Qualifications provides a realistic and broad opportunity for Learners seeking career and professional development. They will support Learners in realising their potential and by association the prospects of the organisations they work with or for. The issues and concepts dealt with as part of this suite of Qualifications are best explored through exposure to organisations, for any full-time Learners work placements are encouraged so that genuine experience and insight can be gained. Problem solving and creativity are attributes encouraged and developed in Learners through all the Units."
      },
      {
        title: "QUALIFI LEVEL 7 DIPLOMA IN EXECUTIVE MANAGEMENT",
        overview:
          "This suite of Qualifications provides a realistic and broad opportunity for Learners seeking career and professional development. They will support Learners in realising their potential and by association the prospects of the organisations they work with or for. The issues and concepts dealt with as part of this suite of Qualifications are best explored through exposure to organisations, for any full-time Learners work placements are encouraged so that genuine experience and insight can be gained. Problem solving and creativity are attributes encouraged and developed in Learners through all the Units."
      },
      {
        title: "QUALIFI LEVEL 8 DIPLOMA IN STRATEGIC MANAGEMENT AND LEADERSHIP",
        overview:
          "This suite of Qualifications provides a realistic and broad opportunity for Learners seeking career and professional development. They will support Learners in realising their potential and by association the prospects of the organisations they work with or for. The issues and concepts dealt with as part of this suite of Qualifications are best explored through exposure to organisations, for any full-time Learners work placements are encouraged so that genuine experience and insight can be gained. Problem solving and creativity are attributes encouraged and developed in Learners through all the Units."
      }
    ]
  }),
  components: {
    Program
  }
};
</script>

<style lang="scss" scoped>
#programHeading {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 30vh;
}
#screen3 {
  min-height: 30vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.basil {
  background-color: #fffbe6 !important;
}
.basil--text {
  color: #356859 !important;
}
</style>
