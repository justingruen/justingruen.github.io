<template>
  <div>
    <div
      id="dark-start"
      :style="{ backgroundColor: darkStartBackgroundColor }"
      :class="{ transition: darkStartTransition }"
    ></div>
    <div id="vanta" class="stationary-background"></div>
    <div class="container">
      <div class="full-title">
        <div class="profile">
          <img src="../static/Me.png" class="profile-pic" alt="Justin Gruen" />
        </div>
        <h1
          id="typing-title"
          class="display-4"
          :style="{ zIndex: typingTitleZIndex, color: typingTitleColor }"
          @click="onTitleClick"
        >
          <span class="title">{{ titleText }}</span>
        </h1>
        <div>
          <span>
            <a href="#" @click="popupEmail">Email</a>
          </span>
          •
          <span>
            <a target="_blank" href="https://www.linkedin.com/in/justingruen/"
              >LinkedIn</a
            >
          </span>
          <br />
          <span>
            <a target="_blank" href="JustinGruen.pdf">Resume</a>
          </span>
          •
          <span>
            <a
              target="_blank"
              href="https://open.spotify.com/user/dja6299?si=xo7Pb8jtTGW2HEFK8YXpAA"
              >Spotify</a
            >
          </span>
          •
          <span>
            <a target="_blank" href="https://github.com/justingruen/">Github</a>
          </span>
          <!-- <listening /> -->
        </div>
      </div>

      <!-- Rutgers Position -->
      <div id="project-cards" :class="{ nonexistent: projectCardsNonexistent }">
        <div class="row">
          <div class="col-md-6 card-col" style="justify-content: center;">
            <div class="card" style="width: 50em;">
              <div class="card-block">
                <div class="card-title" style="margin-top: 1.5em 0;">
                  <img
                    class="company-logo"
                    src="../static/rutgers-logo.svg"
                    style="width: 9em; margin: .3em 0;"
                  />
                </div>
                <div class="row">
                  <div class="col-lg-12">
                    <div style="margin:1em;">
                      <h5 class="card-subtitle">Full Stack Engineer</h5>
                      <div class="card-text">
                        September 2022 - Present
                      </div>

                      <div class="card-buttons">
                        <button
                          type="button"
                          class="btn btn-outline-dark"
                          @click="popupWAD"
                        >
                          More Info
                        </button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Comcast Position -->
          <div class="col-md-6 card-col" style="justify-content: center;">
            <div class="card" style="width: 50em;">
              <div class="card-block">
                <div class="card-title" style="margin-top: 1.5em 0;">
                  <img
                    class="company-logo"
                    src="../static/comcast-logo.svg"
                    style="width: 9em; margin: .3em 0;"
                  />
                </div>
                <div class="row">
                  <div class="col-lg-12">
                    <div style="margin:1em;">
                      <h5 class="card-subtitle">Front End Developer</h5>
                      <div class="card-text">
                        April 2021 - September 2022
                      </div>

                      <div class="card-buttons">
                        <button
                          type="button"
                          class="btn btn-outline-dark"
                          @click="popupSDI"
                        >
                          More Info
                        </button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="row">
          <!-- <div class="col-md-2"></div> -->
          <div class="col-md-12 card-col" style="justify-content: center;">
            <div class="card" style="width: 60em;">
              <div class="card-block">
                <div class="card-title" style="margin-top: 1.5em 0;">
                  <img
                    class="company-logo"
                    src="../static/wac-logo.svg"
                    style="width: 9em; margin: .3em 0;"
                  />
                </div>
                <div class="row">
                  <div class="col-lg-6">
                    <div style="margin:1em;">
                      <h5 class="card-subtitle">Front End Developer</h5>
                      <div class="card-text">
                        August 2020 - December 2020
                      </div>

                      <div class="card-buttons">
                        <button
                          type="button"
                          class="btn btn-outline-dark"
                          @click="popupGJM"
                        >
                          More Info
                        </button>
                      </div>
                    </div>
                  </div>
                  <div class="col-lg-6">
                    <div style="margin:1em;">
                      <h5 class="card-subtitle">
                        Applications Developer
                      </h5>
                      <div class="card-text">August 2019 - August 2020</div>

                      <div class="card-buttons">
                        <button
                          type="button"
                          class="btn btn-outline-dark"
                          @click="popupGSA"
                        >
                          More Info
                        </button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <!-- <div class="col-md-2"></div> -->
        </div>

        <!-- <div class="row">
          <project-card
            title="GeoEvent Server"
            left-button-href=""
            left-button-text=""
            right-button-href=""
            right-button-text="View on GitHub"
          >
            Text here
          </project-card>

          <project-card
            title="IW Equipment Scheduling System"
            left-button-href=""
            left-button-text=""
            right-button-href=""
            right-button-text="View on GitHub"
          >
            Text here
          </project-card>
        </div> -->

        <br />
        <br />
        <div class="row">
          <project-card
            title="Classroom Helper Discord Bot"
            left-button-href="https://discord.com/api/oauth2/authorize?client_id=751089692153348118&permissions=0&scope=bot"
            left-button-text="Try it Out"
            right-button-href="https://github.com/justingruen/teacher-helper"
            right-button-text="View on GitHub"
          >
            Due to the Covid-19 pandemic, a lot of my professors began teaching
            using Discord. The bot they were using to manage students was buggy
            though, so I offered to make my own. It mainly moves students
            between voice channels but offers a few extra helpful commands as
            well.
          </project-card>
          <project-card
            title="Record Top Records"
            left-button-href="http://www.justingruen.com/recordtoprecords/"
            left-button-text="Check it out!"
            right-button-href="https://github.com/justingruen/recordtoprecords/tree/master"
            right-button-text="View on Github"
            extra-button-href="cs-sce.pdf"
            extra-button-text="Read about it"
          >
            Record Top Records is a full e-commerce application developed for my
            computer science major SCE. The software was developed using React,
            Nodejs, Google Firebase, Material-UI, and Stripe. Users can create
            their own accounts, view the product catalog, add items to the cart,
            and more.
          </project-card>
        </div>
        <div class="row">
          <project-card
            title="Cooking Timer App"
            left-button-href="https://github.com/justingruen/cookingtimer"
            left-button-text="View on Github"
            right-button-href=""
            right-button-text="View on Github"
          >
            An android application meant to help track time while I cook by
            allowing me to create intervals rather than just having to use a
            single timer.
          </project-card>
          <project-card
            title="Custom Role-Provider Discord Bot"
            left-button-href="https://discord.com/api/oauth2/authorize?client_id=764122203922628608&permissions=268512368&scope=bot"
            left-button-text="Try it Out"
            right-button-href="https://github.com/justingruen/esports-bot"
            right-button-text="View on Github"
          >
            My school's esports discord server uses roles to easily manage
            teams. Instead of paying for the Mee6 bot premium that can easily
            give users roles, I offered to build my own. It allows
            administrators to create posts with emojis that students can click
            on to automatically gain a role.
          </project-card>
        </div>
        <div class="row">
          <project-card
            title="Fetch"
            left-button-href="https://github.com/justingruen/fetch"
            left-button-text="View on Github"
            right-button-href=""
            right-button-text="View on GitHub"
          >
            A 2D cooperative puzzle platformer developed in Unity about two dogs
            trying to return a ball to their owner. Each level attempts to
            utilize new mechanics presented to the player to assist them on
            their journey.
          </project-card>
          <project-card
            title="Video Us"
            left-button-href="https://github.com/justingruen/videous"
            left-button-text="View on Github"
            right-button-href=""
            right-button-text=""
          >
            I frequently enjoy watching movies with friends, and decided to try
            creating my own video watching web app. Video Us is an application
            that allows users to create rooms, invite friends, and synchronously
            play videos at the touch of a button.
          </project-card>
        </div>
        <div>
          <project-card
            title="Headphone Price Tracker"
            left-button-href=""
            left-button-text="Under Construction!"
            right-button-href=""
            right-button-text=""
          >
            Quality headphones can get extremely expensive, and except for the
            r/Headphones subreddit, there's no way to easily view headphone
            prices and check what's on sale. This website is intended to take in
            user-submitted links, retrieve the current price, and provide
            various information to the user to help them make an informed
            decision.
          </project-card>
        </div>

        <br />
        <footer>
          justingruen,
          <span id="footer-year">{{ year }}</span>
          <br />
          <a
            href="https://github.com/justingruen/justingruen.github.io"
            target="_blank"
            >View on GitHub</a
          >
        </footer>
      </div>
    </div>
    <!-- /.container -->
  </div>
</template>

<script>
import Cookies from 'js-cookie'
import Typed from 'typed.js'
import Swal from 'sweetalert2'

// import Listening from '~/components/Listening.vue'  // Still under construction
import ProjectCard from '~/components/ProjectCard.vue'

const Popup = Swal.mixin({
  confirmButtonColor: '#7c9cff'
})

export default {
  // components: { Listening, ProjectCard },
  components: { ProjectCard },
  data: () => ({
    year: new Date().getFullYear(),
    titleText: '',
    typingTitleZIndex: () => 100,
    typingTitleColor: () => 'white',
    projectCardsNonexistent: true,
    darkStartBackgroundColor: '#212529',
    darkStartTransition: false
  }),
  mounted() {
    const shouldPlayAnimation = !(Cookies.get('typed') === 'true')

    const sixteenHours = 16 / 24
    Cookies.set('typed', 'true', { expires: sixteenHours })

    if (shouldPlayAnimation) {
      // start the title above the shadow, and as white text
      this.typingTitleZIndex = 100
      this.typingTitleColor = 'white'

      // execute the animation
      new Typed('.title', {
        strings: ['Justin Gruen'],
        typeSpeed: 100,
        onComplete: () => {
          // wait a bit, then show the page
          setTimeout(() => this.showPage(), 300)
        }
      })
    } else {
      // forgo the animation, and just show the page
      this.titleText = 'Justin Gruen'
      this.showPage()
    }
  },
  methods: {
    showPage() {
      // make the elements take up space by removing
      // display: none, without removing opacity 0
      this.projectCardsNonexistent = false

      // get rid of the solid color covering the page
      this.darkStartBackgroundColor = 'transparent'

      // invert title text color
      this.typingTitleColor = '#212529'

      // begin the circle transition
      this.darkStartTransition = true
    },
    popupEmail() {
      Popup.fire({
        title: 'Email me!',
        html:
          '<div style="color: light-blue; text-align:center;"><a href="mailto:justinmgruen0@gmail.com">justinmgruen0@gmail.com</a></div>'
      })
    },

    popupWAD() {
      const innerHTML =
        '<p>Working as a Web Applications Developer as part of the Rutgers Continuing Studies Division is my most recent and current role! ' +
        "Due to our small team size, I'm able to take on more of an independent role in software development. This means designing our " +
        "product's roadmap, making major decisions on how we want the user to interact with our applications, and being responsible for developing larger " +
        "pieces of the frontend and backend infrastructure! Here's what I put on my resume about it: <br><br>" +
        '<ul style="text-align: left;"><li> Led development of a recruiting platform employed across 34 departments, overseeing timely feature delivery, custom UI/UX implementation, and resilient back end architecture.</li>' +
        '<li>Created, tested, and modified a library of common React components using Storybook, Typescript, and Tailwind CSS for use in existing codebases.</li>' +
        '<li> Composed a feature roadmap and introduced Agile methodologies through the implementation of a user story pipeline, increasing code quality and speed of delivery.</li>' +
        '<li> Interfaced with design team to create prototypes of major and minor features, alongside ensuring compliance with ADA standards</li>' +
        '</ul></p>'
      Popup.fire({
        html: innerHTML,
        imageUrl: ''
      })
    },

    // Finally, towards the end of my time there, as our platform grew and we were receiving end user support requests at an increased rate, ' +
    // 'I designed a future in-house Contact-Us application for our sales team to quickly look up solutions or ask us questions without using a messy Slack channel as an intermediary

    popupSDI() {
      const innerHTML =
        '<p>For my first major development role as part of a larger org, I was able to become part of an amazing team over at Comcast Business. ' +
        'Originally I used Angular and Jasmine to help to build an automation platform for customers to set-up defined networks with. As time went on though, I was able to assist in backend user stories as well, ' +
        "learning Java and Springboot to be able to take on more work. Finally towards the end of my time there, while I was able to do so much more, the part I'm proudest of was taking on a mentorship role for two of our junior developers, " +
        "assisting them in learning our application's architecture and generally helping them grow. Here's what I have to say on my resume about it: <br><br>" +
        '<ul style="text-align: left;"><li> Leveraged CI/CD pipelines to prototype an in-house application to simplify weekly deployments, reducing deployment overhead, minimizing downtime, and increasing app availability.</li>' +
        '<li>Provisioned components and bug fixes across three Angular codebases, and RESTful API’s across multiple Java microservices.</li>' +
        '<li>Trained and mentored junior engineers joining the team, working with them through pair programming and weekly one-on-one meetings.</li>' +
        '<li> Achieved a 50% reduction in user support tickets and developer maintenance through integration of testing suites for both front end and back end codebases.</li>' +
        '<li>Provided end users around the clock support ensuring that in-app issues are resolved in a timely fashion, reducing total customer impact or delay by ~12 hours weekly</li>' +
        '</ul></p>'
      Popup.fire({
        html: innerHTML,
        imageUrl: ''
      })
    },

    popupGJM() {
      const innerHTML =
        '<p>After being from promoted from general applications developer to front end developer, I was able to work directly with the senior engineer in a larger capacity. ' +
        'I shifted from working primarily with Python and Arcpy to working with Javascript, React, and front end development,' +
        " as well as more in-depth backend development for our GeoEvent Server! Here's just a few of the things I was able to do: <br><br>" +
        '<ul style="text-align: left;"><li>Designed and built a vehicle crash tracker application using React and the ArcGIS API, enabling emergency responders to easily process, filter, and view 15+ years of Maryland crash data.</li>' +
        '<li>Prototyped an in-house web application for 25+ authenticated users to submit and view location data in GeoJSON files using JavaScript, HTML, CSS, and the Google Maps API.</li>' +
        '<li>Collaborated with GIS analysts to automate manual processes and increase deliverables production by ~20%.</li>' +
        '</ul></p>'
      Popup.fire({
        html: innerHTML,
        imageUrl: ''
      })
    },

    popupGSA() {
      const innerHTML =
        "<p>My first major role was as an applications developer with Washington College's GIS Labs. I started out analyzing data ​" +
        "using Python and Arcpy, Esri's Python library, and quickly moved to creating full scale python scripts to easily automate " +
        'a large amount of data processing. During the summer of 2020 I began working with Sean Lynn, the senior web developer, ' +
        ' and shifted to developing backend data-processing and MySQL database storage for our GeoEvent server. ' +
        " Here's just a few of the things I was able to do:<br><br>" +
        '<ul style="text-align: left;"><li>Independently responsible for creating, maintaining, and continuously expanding a toolbox containing 20+ user-friendly geoprocessing Python tools and software that sifts, analyzes, and displays data findings in multiple formats.</li>' +
        '<li>Collaborated with GIS analysts to automate manual processes and increase deliverables production by ~10%.</li>' +
        '<li>Redesigned UI options on existing geospatial analysis scripts to adhere to a wider range of needs.</li>' +
        '</ul></p>'
      Popup.fire({
        html: innerHTML,
        imageUrl: ''
      })
    },

    onTitleClick() {
      if (this.projectCardsNonexistent) {
        // forgo the animation, and just show the page
        this.titleText = 'Justin Gruen'
        this.showPage()
      } else {
        this.popupReplayAnimation()
      }
    },

    popupReplayAnimation() {
      Popup.fire({
        title: 'Want to see the typing intro animation again?',
        type: 'question',
        showCancelButton: true,
        confirmButtonText: 'Yes',
        cancelButtonText: 'No'
      }).then((result) => {
        if (result.value) {
          Cookies.set('typed', 'false')
          location.reload()
        }
      })
    }
  }
}
</script>

<style>
/*
 *	Main
 */
body {
  padding-bottom: 2rem;
  color: #212529;
  text-align: center;
}

.gradient-background {
  background-image: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.stationary-background {
  background: #7c9cff;
  background-repeat: no-repeat;
  width: 100%;
  top: -80px;
  bottom: -80px;
  position: fixed;
  z-index: -1;
}

#dark-start {
  opacity: 1;
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0px;
  left: 0px;
  z-index: 1;
  pointer-events: none;
}

#dark-start:before {
  content: '';
  position: fixed;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  border-radius: 100%;
  animation-duration: 1s;
  box-shadow: 0px 0px 0px 100vmax #212529;
  width: 150vmax;
  height: 150vmax;
}

.transition:before {
  animation-name: spotlight;
}

.nonexistent {
  display: none;
}

@keyframes spotlight {
  from {
    width: 0vmin;
    height: 0vmin;
  }

  to {
    width: 150vmax;
    height: 150vmax;
  }
}

/*
 *	Header
 */
.full-title {
  padding-top: 0.5rem;
  padding-bottom: 1rem;
  font-size: 1.1rem;
}

.profile {
  display: inline-block;
  margin: 1rem 0;
}

.profile-pic {
  height: 180px;
  border-radius: 50%;
}

.breathe::before {
  content: '';
  position: absolute;
  z-index: -1;
  height: 130px;
  width: 130px;
  border-radius: 50%;
  box-shadow: inset 0 0 0 16px rgba(0, 0, 0, 0.3);
  animation: breathe 16s infinite;
}

@keyframes breathe {
  from,
  75%,
  to {
    transform: scale(1, 1);
  }

  25%,
  50% {
    transform: scale(1.25, 1.25);
  }
}

.full-title a,
a:active,
a:visited {
  display: inline-block;
  color: #212529;
  transition: all 0.2s ease-in-out;
}

a:hover {
  transform: scale(1.05);
}

body {
  font-family: 'Jost', sans-serif;
  font-weight: 400;
}

.full-title .display-4 {
  font-family: 'Jost', sans-serif;
  font-weight: 500;
  font-size: 2.5em;
}

span.avoidwrap {
  display: inline-block;
}

#typing-title {
  position: relative;
  margin-bottom: 12px;
  transition: all 0.2s ease-in;
}

.company-logo {
  max-width: 62.5%;
  max-height: 105px;
}

/* fix line appearing between buttons */
.card a:hover {
  color: transparent;
}

.card-buttons {
  margin-top: 0.8em;
}

.btn-outline-dark {
  color: #212529;
  border-color: #212529;
  margin-bottom: 0.3em;
}

/*
 *	SweetAlert
 */
#swal2-content {
  text-align: left;
  font-weight: normal;
}

#swal2-content a {
  color: #45c299;
}

#swal2-content a:hover {
  text-decoration: underline;
}

.swal2-image {
  margin-top: -1.25em;
  margin-left: -1.25em;
  max-width: calc(100% + 2.5em);
  border-radius: 5px 5px 0px 0px;
}

/*
 *	Typed.js
 */
.typed-cursor {
  opacity: 1;
  -webkit-animation: blink 0.7s infinite;
  -moz-animation: blink 0.7s infinite;
  animation: blink 0.7s infinite;
}

@keyframes blink {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
