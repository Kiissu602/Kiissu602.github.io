<template>
  <div>
    <v-parallax height="300" :src="require(`~/assets/para.jpg`)"></v-parallax>
    <div class="d-flex justify-center">
      <v-avatar class="ava" size="220">
        <img
          :src="require(`~/assets/profile.jpg`)"
          alt="Pichai Namwan Profile Picture"
        />
      </v-avatar>
    </div>
    <div class="d-flex justify-center">
      <h1 class="name text-h4 mt-4">Pichai Namwan</h1>
    </div>
    <div class="d-flex justify-center">
      <p class="uni text-h5 mt-2 deep-purple--text text--darken-2">
        Chiang Mai University Student
      </p>
    </div>
    <v-container class="content">
      <v-divider class="fline grey darken-2 my-4" />
      <v-row>
        <v-col>
          <p class="prof text-h6 text-center text-subtitle-1">Profile</p>
        </v-col>
      </v-row>
      <v-row v-for="(i, index) in profile" :key="index">
        <v-col offset="2" sm="3">
          <p class="det text-right text-subtitle-1">{{ i.tag }}</p>
        </v-col>
        <v-col offset="1">
          <p class="text-subtitle-1">
            <a class="click" :href="i.link" target="_blank">{{ i.dat }}</a>
          </p>
        </v-col>
      </v-row>
      <v-divider class="fline grey darken-2 my-4" />
      <v-row class="mt-4">
        <v-col>
          <p class="skll text-h6 text-center text-subtitle-1">Skill</p>
        </v-col>
      </v-row>
      <v-row>
        <v-col v-for="i in skill" :key="i" cols="6"
          ><p class="text-center text-subtitle-1">{{ i }}</p>
        </v-col>
      </v-row>
      <v-divider class="fline grey darken-2 my-4" /><v-row>
        <v-col>
          <p class="proj text-h6 text-center text-subtitle-1">Project</p>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-card>
            <v-parallax
              height="150"
              :src="require(`~/assets/prog.png`)"
            ></v-parallax>
            <v-card-title
              ><a
                class="click"
                href="https://github.com/Kiissu602/ProGReviews"
                target="_blank"
                >ProGReviews</a
              ></v-card-title
            >
            <v-card-text>Vue.js</v-card-text>
          </v-card>
        </v-col>
        <v-col>
          <v-card>
            <v-parallax
              height="150"
              :src="require(`~/assets/java.png`)"
            ></v-parallax>
            <v-card-title>
              <a
                class="click"
                href="https://github.com/Kiissu602/BombServive"
                target="_blank"
                >BombServive</a
              ></v-card-title
            ><v-card-text>Java</v-card-text>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-card>
            <v-parallax
              height="150"
              :src="require(`~/assets/database.png`)"
            ></v-parallax>
            <v-card-title> LibrarySystemManagement</v-card-title>
            <v-card-text>Vue.js, C#</v-card-text>
            <v-row no-gutters>
              <v-col no-gutters>
                <v-card-actions
                  ><v-btn
                    class="click"
                    href="https://github.com/Kiissu602/204321-client-project"
                    target="_blank"
                    text
                    >Frontend</v-btn
                  >
                </v-card-actions>
              </v-col>
              <v-col no-gutters>
                <v-card-actions
                  ><v-btn
                    class="click"
                    href="https://github.com/Kiissu602/204321-server-project"
                    target="_blank"
                    text
                    >Backend</v-btn
                  >
                </v-card-actions>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col> </v-col>
      </v-row>
      <v-divider class="fline grey darken-2 my-4" />
      <v-row class="mt-4">
        <v-col>
          <p class="edu text-h6 text-center text-subtitle-1">Education</p>
          <v-col>
            <p class="text-center text-subtitle-1">Chaing Mai University</p>
            <br />
            <p class="text-center text-subtitle-1">
              3rd year Computer Science student
            </p>
            <br />
            <p class="text-center text-subtitle-1">Current GPA 2.44</p>
            <br />
            <p class="text-center text-subtitle-1">
              Business Administration Minor Subject
            </p>
            <br />
            <p class="text-center text-subtitle-1">
              Vice President Of The Department
            </p>
          </v-col>
        </v-col>
      </v-row>
      <v-divider class="fline grey darken-2 my-4" />
      <v-row>
        <v-col>
          <p class="exp text-h6 text-center text-subtitle-1">Experience</p>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <p class="day text-center text-subtitle-1">
            5 Days Major Camp TuTor 2020
          </p>
        </v-col>
      </v-row>
      <v-row no-gutters>
        <v-col offset="2">
          <p class="text-center text-subtitle-1">
            - Teach some Angular topic to freshmen
          </p>
        </v-col>
      </v-row>
      <v-divider class="fline grey darken-2 my-4" />
    </v-container>
    <link href="style.css" rel="stylesheet" type="text/css" media="print" />
  </div>
</template>

<script>
export default {
  data: () => ({
    profile: [
      {
        tag: 'Name:',
        dat: 'Pichai Namwan',
        link: 'https://www.facebook.com/poolmean.devil/',
      },
      {
        tag: 'Email:',
        dat: 'pichai.namwan602@gmail.com',
        link: 'mailto:pichai.namwan602@gmail.com',
      },
      {
        tag: 'Phone:',
        dat: '+66932895079',
        link: 'tel:+66932895079',
      },
      {
        tag: 'Github:',
        dat: 'github.com/Kiissu602',
        link: 'https://github.com/Kiissu602',
      },
    ],
    skill: [
      'HTML/CSS',
      'JavaScript',
      'Vue.js',
      'ASP.NET Core',
      'SQL Database',
      'Entity Framework Core',
      'Git',
      'Python',
      'Datavisualization',
      'Java',
      'C/C++',
      'Android',
    ],
  }),
}
</script>

<style scoped>
.ava {
  margin-top: -110px;
}
.sline {
  margin: 0 600px;
}
.content {
  max-width: 680px;
}
.click {
  color: rgba(0, 0, 0, 0.87);
  text-decoration: none;
}
.click:hover {
  color: #5e35b1;
}

.prof,
.skll,
.edu,
.exp,
.proj {
  font-weight: 600;
  color: #7b1fa2;
}
.det,
.day {
  font-weight: 500;
}
</style>
