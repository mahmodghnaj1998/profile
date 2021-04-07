<template>
  <div>
    <v-row>
      <v-img src="/1.png" height="655">
        <v-container class="fill-height align-end justify-end">
          <v-row class="align-end justify-end text-right" no-gutters>
            <p class="text-uppercase display-3">Mahmod Ghnaj</p>
            <h1 class="primary--text text-uppercase display-4">
              FullStack Developer
            </h1>
          </v-row>
        </v-container>
      </v-img>
      <v-container fluid>
        <v-row>
          <v-img :src="url">
            <v-row id="about" class="mt-14 ml-4">
              <v-col cols="12" md="12">
                <h1 class="primary--text font-weight-bold display-2">
                  Who I am..
                </h1>
              </v-col>
              <v-col cols="12" md="7" class="justify-space-between mt-5">
                <v-row>
                  <v-col cols="12" md="7" class="mb-5 mb-0">
                    Full Stack Developer with 2+ years of hands-on experience
                    designing, developing, and implementing applications and
                    solutions using a range of technologies and programming
                    languages. Seeking to leverage broad development experience
                    and hands-on technical expertise in a challenging role as a
                    Full-stack Develope
                  </v-col>
                  <v-col cols="12" md="4">
                    <v-row class="align-center">
                      <v-col
                        cols="12"
                        md="6"
                        class="text-uppercase primary--text font-weight-medium"
                      >
                        <div class="mb-3">Location</div>
                        <div class="mb-3">Email</div>
                        <div class="mb-3">Phone</div>
                      </v-col>
                      <v-col cols="12" md="6" class="subheading text-no-wrap">
                        <div class="mb-3">Syria</div>
                        <div class="mb-3">mahmodghnaj1@gmail.com</div>
                        <div class="mb-3">(963) 934-952-316</div>
                      </v-col>
                    </v-row>
                  </v-col>
                </v-row>
              </v-col>
              <v-col
                cols="12"
                md="5"
                class="hidden-sm-and-down text-right text-uppercase"
              >
                <div class="display-1 pa-2">FullStack Developer</div>
                <div class="primary--text headline font-weight-light pa-2">
                  Mahmod Ghnaj
                </div>
              </v-col>
            </v-row>
            <v-row id="service" class="mt-4 ml-4">
              <v-col cols="12" md="6">
                <h1 class="primary--text font-weight-bold display-2">
                  What I can do for you.
                </h1>
                <v-expansion-panels inset class="mt-5">
                  <v-expansion-panel v-for="(item, i) in item" :key="i">
                    <v-expansion-panel-header class="title font-weight-light">{{
                      item.titile
                    }}</v-expansion-panel-header>
                    <v-expansion-panel-content>
                      {{ item.decs }}
                    </v-expansion-panel-content>
                  </v-expansion-panel>
                </v-expansion-panels>
              </v-col>
              <v-col cols="12" md="6">
                <v-img src="/d.png"></v-img>
              </v-col>
            </v-row>
            <v-row id="experience" class="mt-4 ml-4">
              <h1 class="primary--text font-weight-bold display-2">
                Where I've been
              </h1>
              <v-timeline>
                <v-timeline-item
                  v-for="n in years"
                  :key="n.years"
                  large
                  color="orange"
                  fill-dot
                >
                  <template v-slot:opposite>
                    <span>{{ n.year }}</span>
                  </template>
                  <v-card class="elevation-2">
                    <v-card-title class="headline"> FreeLancer </v-card-title>
                    <v-card-text class="subheading font-weight-bold">
                      {{ n.des }}
                    </v-card-text>
                  </v-card>
                </v-timeline-item>
              </v-timeline>
            </v-row>
            <v-row id="skills" class="mt-4 ml-4">
              <h1 class="primary--text font-weight-bold display-2">
                What I know..
              </h1>
            </v-row>
            <v-row class="mt-4 ml-4 justify-space-around">
              <v-col cols="12" md="3" class="mb-6 mt-8">
                <h3 class="headline font-weight-medium mb-4 primary--text">
                  My Education
                </h3>
                <v-sheet
                  color="grey darken-2"
                  elevation="1"
                  height="200"
                  shaped
                  width="300"
                >
                  <v-row>
                    <v-col cols="12" class="">
                      <h4 class="title text-center primary--text">
                        BA in Computer technology
                      </h4>
                      <v-footer color="grey darken-2">
                        <p>2015-2020</p>
                      </v-footer>
                      <v-footer color="grey darken-2">
                        <p>University of Hama ,syria</p>
                      </v-footer>
                    </v-col>
                  </v-row>
                </v-sheet>
              </v-col>
              <v-col cols="12" md="4" class="mb-6 mt-8 justify-space-around">
                <h3 class="headline font-weight-medium mb-4 primary--text">
                  My Skills
                </h3>
                <h4 class="text-uppercase mb-3 primary--text">Programming</h4>
                <v-row class="mb-2">
                  <v-col cols="12" md="4">
                    <h4 class="subheader">Laravel/php</h4>
                  </v-col>
                  <v-col cols="12" md="4">
                    <v-rating
                      v-model="rating"
                      background-color="orange"
                      color="orange"
                      dense
                    ></v-rating>
                  </v-col>
                </v-row>
                <v-row class="mb-2">
                  <v-col cols="12" md="4">
                    <h4 class="subheader">MySQL</h4>
                  </v-col>
                  <v-col cols="12" md="4">
                    <v-rating
                      v-model="rating"
                      background-color="orange"
                      color="orange"
                      dense
                    ></v-rating>
                  </v-col>
                </v-row>
                <v-row class="mb-2">
                  <v-col cols="12" md="4">
                    <h4 class="subheader">JavaScript</h4>
                  </v-col>
                  <v-col cols="12" md="4">
                    <v-rating
                      v-model="rating"
                      background-color="orange"
                      color="orange"
                      dense
                    ></v-rating>
                  </v-col>
                </v-row>
                <v-row class="mb-2">
                  <v-col cols="12" md="4">
                    <h4 class="subheader">Vuejs/Vuetifyjs</h4>
                  </v-col>
                  <v-col cols="12" md="4">
                    <v-rating
                      v-model="rating"
                      background-color="orange"
                      color="orange"
                      dense
                    ></v-rating>
                  </v-col>
                </v-row>
                   <v-row class="mb-2">
                  <v-col cols="12" md="4">
                    <h4 class="subheader">Nuxtjs</h4>
                  </v-col>
                  <v-col cols="12" md="4">
                    <v-rating
                      v-model="rating"
                      background-color="orange"
                      color="orange"
                      dense
                    ></v-rating>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
            <v-row id="project" class="mt-4 ml-4">
              <h1 class="primary--text font-weight-bold display-2">Projects</h1>
              <v-row align="center" class="mt-4 mb-4">
                <v-col>
                  <v-window v-model="window" class="elevation-1" vertical>
                    <v-window-item v-for="n in projects" :key="n.id">
                      <v-card flat color="grey darken-2">
                        <v-card-text>
                          <v-row class="mb-4" align="center">
                            <strong class="title">{{ n.title }}</strong>
                          </v-row>

                          <p v-html="n.desc"></p>
                          <v-expansion-panels inset class="mt-5">
                            <v-expansion-panel>
                              <v-expansion-panel-header
                                class="title font-weight-light"
                              >
                                Show Details
                              </v-expansion-panel-header>
                              <v-expansion-panel-content>
                                <v-carousel hide-delimiters>
                                  <v-carousel-item
                                    v-for="n in n.project"
                                    :key="n.id"
                                  >
                                    <v-card color="grey">
                                      <v-row
                                        class="fill-height"
                                        align="center"
                                        justify="center"
                                      >
                                        <v-img
                                          height="500"
                                          width="1000"
                                          :src="n.src"
                                        ></v-img>
                                      </v-row>
                                    </v-card>
                                  </v-carousel-item>
                                </v-carousel>
                              </v-expansion-panel-content>
                            </v-expansion-panel>
                          </v-expansion-panels>
                        </v-card-text>
                      </v-card>
                    </v-window-item>
                  </v-window>
                  <v-item-group v-model="window" class="text-center" mandatory>
                    <v-item
                      v-for="n in projects"
                      :key="n.id"
                      v-slot="{ active, toggle }"
                    >
                      <v-btn
                        :input-value="active"
                        icon
                        @click="toggle"
                        color="grey darken-2"
                      >
                        <v-icon>mdi-record</v-icon>
                      </v-btn>
                    </v-item>
                  </v-item-group>
                </v-col>
              </v-row>
            </v-row>
            <v-row id="conect" class="mt-4 ml-4 mb-7">
              <v-col cols="12" md="12" class="mb-4">
                <h1 class="primary--text font-weight-bold display-2">
                  Let's talk.
                </h1>
              </v-col>
              <v-col cols="12" md="5">
                <h2
                  class="primary--text title font-weight-light text-uppercase"
                >
                  What can I do for you?
                </h2>
                <div class="subheading mb-5 mb-5">
                  Help you find a meaningful website that appears on the web.
                  ... You can create a website using the latest technology and
                  help you show it in search engines
                </div>
                <v-col cols="12">
                  <v-text-field label="Name" outlined></v-text-field>
                </v-col>
                <v-col cols="12">
                  <v-text-field label="Email" outlined></v-text-field>
                </v-col>
                <v-col cols="12">
                  <v-text-field label="subject" outlined></v-text-field>
                </v-col>
                <v-col cols="12">
                  <v-textarea
                    label="Message"
                    auto-grow
                    outlined
                    rows="3"
                    row-height="35"
                    shaped
                  ></v-textarea>
                  <v-btn color="orange"> Contact Me </v-btn>
                </v-col>
              </v-col>
              <v-col cols="12" md="7" class="mb-6">
                <h2
                  class="primary--text title font-weight-light text-uppercase mb-5"
                >
                  SOCIAL CONTACTS
                </h2>
                <v-btn
                  elevation="2"
                  icon
                  large
                  href="https://www.facebook.com/mahmod.ghnaj/"
                >
                  <v-icon medium color="orange">mdi-facebook</v-icon>
                </v-btn>
                <v-btn
                  elevation="2"
                  icon
                  large
                  href="https://github.com/mahmodghnaj1998"
                >
                  <v-icon medium color="orange">mdi-github</v-icon>
                </v-btn>
                <v-btn elevation="2" icon large>
                  <v-icon medium color="orange">mdi-linkedin</v-icon>
                </v-btn>
                <v-list-item v-for="(item, i) in itemss" :key="i" class="mt-5">
                  <v-list-item-icon>
                    <v-icon large color="orange" v-text="item.icon"></v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title
                      class="primary--text"
                      v-text="item.text"
                    ></v-list-item-title>
                    <p class="subtitle mt-3 font-weight-light">
                      {{ item.con }}
                    </p>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
            </v-row>
          </v-img>
        </v-row>
      </v-container>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      url:
        "data:image/png;base64,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",
      item: [
        {
          titile: "Web Development",
          decs:
            "Meet with clients or management to discuss the needs and design of a website. Create and test applications for a website. Write code for the website, using programming languages such as HTML or XML. Work with other team members to determine what information the site will contain.",
        },
        {
          titile: "Design",
          decs:
            "As a web designer, my objective is to make a positive impact on clients, co-workers, and the Internet using my skills and experience to design compelling and attractive websites.",
        },
        {
          titile: "Get your website on Google",
          decs:
            "I analyze the sites of competing clients in the same client site activity to see how they advanced search engines I import all the research words that fit the client site activity",
        },
      ],
      years: [
        {
          year: "2019",
          des:
            "Expertise in developing web pages using HTML, CSS, MVC, Object Oriented Java script, ES6,JSON.Good understanding of Document Object Model (DOM) and DOM Functions Responsible for parsing JSON data to & from the server for presentation & storage purposes in the project. The back-end use of Laravel, Mysql Stack to provide RESTful API.",
        },
        {
          year: "2020",
          des:
            "Expertise in strong experience in building web application using the JavaScript MEAN Stack and MERN Stack using Vue JS, Nuxt.JS, Babel+ES6, Vuetify JS and Web - Pack for Single Page Application development",
        },
        {
          year: "2021",
          des:
            "Extensively used GIT for version controlling and regularly pushed the code to GitHub. Expert in designing web applications and web contents utilizing various Search Engine Optimization (SEO) techniques.",
        },
      ],
      rating: 4,
      itemss: [
        { text: "Address", icon: "mdi-map-marker", con: "Syria-Hama" },
        { text: "Email", icon: "mdi-email", con: "mahmodghnaj1@gmail.com" },
        { text: "Phone", icon: "mdi-phone", con: "(+963) 934-952-316" },
      ],
      projects: [
        {
          id: 1,
          title: "Question And Answe",
          desc:
            " Developed a full-stack web application, 'Question And Answer', using vue Question And Answer is an open community for anyone that codes help you get answers to your toughest coding questions,Where was used with the notification system Socket.io and Redis Cache, User's progress is stored on a backend created using laravel and Mysql <br/> Go to link <a href='https://questionandanswer.vercel.app'>Click her</a>",
          project: [
            {
              id: 1,
              src: "/1.jpg",
            },
            {
              id: 2,
              src: "/2.jpg",
            },
            {
              id: 3,
              src: "/3.jpg",
            },
            {
              id: 4,
              src: "/4.jpg",
            },
            {
              id: 5,
              src: "/5.jpg",
            },
            {
              id: 6,
              src: "/6.jpg",
            },
            {
              id: 7,
              src: "/7.jpg",
            },
            {
              id: 8,
              src: "/8.jpg",
            },
            {
              id: 9,
              src: "/9.jpg",
            },
            {
              id: 10,
              src: "/10.jpg",
            },
            {
              id: 11,
              src: "/11.jpg",
            },
            {
              id: 12,
              src: "/12.jpg",
            },
            {
              id: 13,
              src: "/13.jpg",
            },
            {
              id: 14,
              src: "/14.jpg",
            },
            {
              id: 15,
              src: "/15.jpg",
            },
            {
              id: 16,
              src: "/16.jpg",
            },
            {
              id: 17,
              src: "/17.jpg",
            },
            {
              id: 18,
              src: "/18.jpg",
            },
          ],
        },
        {
          id: 2,
          title: "My Diary",
          desc:
            "Developed a full-stack web application, 'My Diary', using Vue that allows users to Registration on the site and saved your diary. User's progress is stored on a backend created using laravel and mySql <br/> Go to link <a href='https://nice-m.herokuapp.com'>Click her</a>",
          project: [
            {
              id: 20,
              src: "/20.png",
            },
          ],
        },
      ],
      window: 0,
    };
  },
  methods: {
    next() {
      this.onboarding1 =
        this.onboarding1 + 1 === this.length ? 0 : this.onboarding1 + 1;
    },
    prev() {
      this.onboarding1 =
        this.onboarding1 - 1 < 0 ? this.length - 1 : this.onboarding1 - 1;
    },
  },
};
</script>

<style scoped>
.v-application .primary--text {
  color: #ffaa00 !important;
  caret-color: #ffaa00 !important;
}
.v-application .primary {
  color: #ffaa00 !important;
  caret-color: #ffaa00 !important;
}
</style>