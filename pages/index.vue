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
          <img src="../static/Me2.png" class="profile-pic" alt="Justin Gruen" />
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
            <a target="_blank" href="justingruen-resume.pdf">Resume</a>
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

      <div id="project-cards" :class="{ nonexistent: projectCardsNonexistent }">
        <div class="row">
          <!-- <div class="col-md-2"></div> -->
          <div class="col-md-12 card-col" style="justify-content: center;">
            <div class="card" style="width: 50em;">
              <div class="card-block">
                <div class="card-title" style="margin-top: 1.5em 0;">
                  <img
                    class="company-logo"
                    src="../static/wac-logo.svg"
                    style="width: 9em; margin: .3em 0;"
                  />
                </div>
                <div class="row">
                  <div class="col-lg-4">
                    <div style="margin:1em;">
                      <h5 class="card-subtitle">GIS Junior Web Developer</h5>
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
                  <div class="col-lg-4">
                    <div style="margin:1em;">
                      <h5 class="card-subtitle">GIS Junior Applications Developer</h5>
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
                  <div class="col-lg-4">
                    <div style="margin:1em;">
                      <h5 class="card-subtitle">Ideaworks Consultant</h5>
                      <div class="card-text">
                        August 2019 - December 2020
                      </div>

                      <div class="card-buttons">
                        <button
                          type="button"
                          class="btn btn-outline-dark"
                          @click="popupIWC"
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
            I frequently enjoy watching movies with friends, and decided
            to try creating my own video watching web app. Video Us is an 
            application that allows users to create rooms, invite friends, 
            and synchronously play videos at the touch of a button.
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

    popupGJM() {
      const innerHTML =
        '<p>Working as a junior web developer at the Washington College GIS Labs was my most recent and interesting internship! ' +
        'After being from promoted from junior applications developer, I was able to work directly with the senior developer in a more leadership role. ' +
        'I shifted from working primarily with Python and Arcpy to working with Javascript, React, and front end development,' +
        "as well as more in-depth backend development for our GeoEvent Server! Here's what I put on my resume about it: <br><br>" +
        '<ul style="text-align: left;"><li>Designed and built a vehicle crash tracker web page using React and the ArcGIS API, enabling emergency responders to easily process, filter, and view 15+ years of Maryland crash data.</li>' +
        '<li>Prototyped a web application for authenticated users to submit and view locations in GeoJSON files using JavaScript, HTML, CSS, and the Google Maps API.</li>' +
        '<li>Achieved a ~5% increase in data retention through a new script using Pandas to process and query incoming JSON data from the Maryland Department of Transportation.</li>' +
        '</ul></p>'
      Popup.fire({
        html: innerHTML,
        imageUrl: ''
      })
    },

    popupGSA() {
      const innerHTML =
        '<p>My second internship was at the Washington College GIS Labs as a junior applications developer. I started out analyzing data ​' +
        "using Python and Arcpy, Esri's Python library, and quickly moved to creating full scale python scripts to easily automate " +
        'a large amount of data processing. During the summer of 2020 I began working with Sean Lynn, the senior applications developer, ' +
        ' and shifted to developing backend data-processing and MySQL database storage for our GeoEvent server. ' +
        " Here's what I put on my resume about it:<br><br>" +
        '<ul style="text-align: left;"><li>Independently responsible for creating, maintaining, and continuously expanding a toolbox containing 20+ user-friendly geoprocessing Python tools and software that sifts, analyzes, and displays data findings in multiple formats.</li>' +
        '<li>Collaborated with GIS analysts to automate manual processes and increase deliverables production by ~10%.</li>' +
        '<li>Redesigned UI options on existing geospatial analysis scripts to adhere to a wider range of needs.</li>' +
        '</ul></p>'
      Popup.fire({
        html: innerHTML,
        imageUrl: ''
      })
    },

    popupIWC() {
      const innerHTML =
        "<p>My first internship took place at my school's engineering center Ideaworks. " +
        'I was primarily responsible for overseeing the use of the equipment and helping   ' +
        "students use the engineering equipment.​ Although it wasn't an official part of the internship, " +
        "I was also able to assist faculty in teaching students engineering principles through fun projects.</p>"
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
  height: 130px;
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
