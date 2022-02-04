<template>
  <q-page>
    <div id="home" class="flex headline-container row q-py-lg">
      <div class="col-2"></div>
      <div class="col-10 flex" style="flex-wrap: nowrap">
        <div class="flex justify-center q-pb-lg" style="flex-direction: column">
          <h1 class="text-h2 text-bold">Marco Reisinger</h1>
          <h2 class="text-h5" style="line-height: 1.8">
            User Experience Design <br />
            Web Development <br />
            Android Development
          </h2>
        </div>
        <div class="full-width">
          <q-img fit="contain" height="80vh" src="/bildPortfolio.png"></q-img>
        </div>
      </div>
    </div>

    <div
      class="row shadow-2 sticky q-py-sm full-width bg-white"
      style="z-index: 1"
    >
      <div class="col-3"></div>
      <div class="flex justify-between col-6">
        <router-link to="" @click="scrollToElement('home')">Home</router-link>
        <router-link to="" @click="scrollToElement('about')">About</router-link>
        <router-link to="" @click="scrollToElement('projects')"
          >Projects</router-link
        >
        <router-link to="" @click="scrollToElement('contact')"
          >Contact</router-link
        >
      </div>
      <div class="col-3"></div>
    </div>

    <div class="row bg-grey-2 q-pt-lg">
      <div class="col-2"></div>
      <div class="col-8">
        <div class="flex">
          <div>
            <h4 id="about">About me</h4>
            <p>
              Hello, I am Marco, {{ getAge() }} years old. I am studying UX
              Design in Ingolstadt.
            </p>
            <p>
              I am a passionate programmer since I was 13 years old. <br />
              I developed a few own projects and worked in several companies
              since 2017.
            </p>
            <p>
              You find my latest projects below. Feel free to contact me anytime
              in the contact section.
            </p>
          </div>
          <div></div>
        </div>

        <div>
          <h4 id="projects">Projects</h4>

          <div class="flex justify-between">
            <div class="text-h5 q-mb-md">
              <span>Mirrads</span>
              <a href="https://mirrads.de" target="_blank">
                <q-badge class="q-ml-sm">
                  <q-icon name="link"></q-icon> Website
                </q-badge>
              </a>
            </div>
            <div>
              <android-badge></android-badge>
              <vue-badge></vue-badge>
            </div>
          </div>
          <div id="mirrads" class="row q-pt-md">
            <div class="col-sm-12 col-md-5 q-pr-md">
              <p>
                Mirrads is a startup from Ingolstadt which sells smart mirros.
              </p>
              <p>
                I am working for Mirrads since January 2019. The company sells
                mirrors which can show digital messages, mostly for digital
                signage reasons. <br />
                <br />To display the videos & images on the mirror we used a
                android tv box and developed our own software. I created the
                whole app by myself for almost one year. We also implemented
                features like face recognition, nfc, barcode scanners and p2p
                connections between the mirrors. <br />
                <br />
                To control the mirrors, we needed to create our own content
                management system (CMS) In 2021 I quit my android development
                and switched to the frontend work for the CMS.
              </p>
              <p>
                I learned the most important skills at Mirrads, like building a
                proper architecture, working in a team and managing tasks
              </p>
            </div>
            <div class="col-sm-12 col-md-7">
              <q-video
                class="rounded-borders full-width"
                src="https://www.youtube.com/embed/Wtd4c2Evfn8"
                :ratio="16 / 9"
              ></q-video>
            </div>
          </div>

          <div class="flex justify-between q-mt-lg">
            <div class="text-h5 q-mb-md">
              <span>GrandEvent</span>
              <a href="https://mirrads.de" target="_blank">
                <q-badge class="q-ml-sm">
                  <q-icon name="link"></q-icon> Video
                </q-badge>
              </a>
            </div>
            <div>
              <xd-badge></xd-badge>
            </div>
          </div>
          <div class="row q-pt-md">
            <div class="col-sm-12 col-md-7">
              <q-video
                class="rounded-borders full-width"
                :ratio="16 / 9"
                src="https://www.youtube.com/embed/XnZqQ0U-rXo"
              ></q-video>
            </div>
            <div class="col-sm-12 col-md-5 q-pl-md">
              <p>
                In the third semester of UXD at the THI we had to create an
                interface for elderly peolpe. We created the app GrandEvent, an
                app where seniors can find nearby events which are especially
                for them.<br /><br />
                Our goal was to find an idea and make the whole process of
                finding the target group, defining personas, designing
                wireframes and finaly screen design. This was a lot of work, we
                worked mostly with Adobe xd for the screen design. In the end we
                had to animate a movie which you also can find here.
              </p>
            </div>
          </div>

          <div class="flex justify-between q-mt-lg">
            <div class="text-h5 q-mb-md">
              <span>Memodia</span>
              <a href="https://memodia.netlify.com" target="_blank">
                <q-badge class="q-ml-sm">
                  <q-icon name="link"></q-icon> Website
                </q-badge>
              </a>
            </div>
            <div>
              <vue-badge></vue-badge>
            </div>
          </div>
          <div class="row q-pt-md">
            <div class="col-sm-12 col-md-5 q-pr-md">
              <p>
                Memodia is my latest self made project. It is a mixture of a
                diary and gallery app. <br /><br />
                Everyone wants to remember nice moments as long and precise as
                possible, but only some people want to write everything in a
                diary. Therefore I developed Memodia, a app where you can create
                a diary based on your images of your gallery. <br />
                <br />
                Your can create albums like in a gallery but with diary like
                entries inside. You can also search for specific entries and
                share them with others.<br /><br />
                Memodia is a webapp build with the Vue.js based on the quasar
                framework. It runs as a website or an app on your smartphone.
              </p>
            </div>
            <div class="col-sm-12 col-md-7"></div>
          </div>

          <div class="flex justify-between q-mt-lg">
            <div class="text-h5 q-mb-md">
              <span>Tourgether</span>
            </div>
            <div>
              <xd-badge></xd-badge>
            </div>
          </div>
          <div class="row q-pt-md">
            <div class="col-sm-12 col-md-7">
              <q-video
                class="rounded-borders full-width"
                :ratio="16 / 9"
                src="https://www.youtube.de/embed/bX2Asj1Ldyo"
              ></q-video>
            </div>

            <div class="col-sm-12 col-md-5 q-pl-md">
              <p>
                Another university project, which we created in the first
                semester. We wanted to create an app where groups of friends
                find together to plan their trip.<br /><br />
                I really liked this idea beacause I already developed a similiar
                project in my sparetime (see
                <a @click="scrollToElement('roundtrips4you')">Roundtrips4you</a
                >). We designed screens in XD and created a final movie of our
                project.<br /><br />
                This project helped me a lot to get the first experience in
                designing screens and developing a product from its idea.
              </p>
            </div>
          </div>

          <div id="roundtrips4you" class="flex justify-between q-mt-lg">
            <div class="text-h5 q-mb-md">
              <span>Roundtrips4you</span>
              <a href="https://roundtrips4you.de" target="_blank">
                <q-badge class="q-ml-sm">
                  <q-icon name="link"></q-icon> Website
                </q-badge>
              </a>
            </div>
            <div>
              <vue-badge></vue-badge>
            </div>
          </div>
          <div class="row q-pt-md">
            <div class="col-sm-12 col-md-5 q-pr-md">
              <p>
                I developed for almost 3 years on my biggest self made Project
                Roundtrips4you.<br />
                The idea behind this vue.js website was to create a platform
                where you can plan and organize your trip.<br /><br />
                I started to use vue.js here for the first time and immediately
                liked it. I also used firebase for the first time to create a
                non sql database. I build a lot of difficult things for
                Roundtrips4you, like a routing service like google maps based on
                mapbox, an authentication system with firebase and a huge trip
                creation software which is very customizeable.
                <br /><br />
                All in all, I got almost my whole vue.js knowledge from
                Roundtrips4you and learned also a lot about modern frameworks
                and techniques.
              </p>
            </div>
            <div class="col-sm-12 col-md-7">
              <q-video
                class="rounded-borders full-width"
                :ratio="16 / 9"
                src="https://youtube.de/embed/YLek64s5ctc"
              ></q-video>
            </div>
          </div>

          <div class="flex justify-between q-mt-lg">
            <div class="text-h5 q-mb-md">
              <span>Memucho</span>
              <a href="https://memucho.de" target="_blank">
                <q-badge class="q-ml-sm">
                  <q-icon name="link"></q-icon> Website
                </q-badge>
              </a>
            </div>
            <div></div>
          </div>
          <div class="row q-pt-md">
            <div class="col-sm-12 col-md-7">
              <q-video
                src="https://youtube.de/embed/NCLgUBGI74I"
                :ratio="16 / 9"
              ></q-video>
            </div>
            <div class="col-sm-12 col-md-5 q-pl-md">
              <p>
                Memucho was the first company where I developed software. It is
                a website where you can learn interesting things very fast and
                share your progress with a community. <br /><br />
                Because the company is from Berlin, I worked completely remote.
                The website is build with C# and asp.net. As I started
                programming with the asp.net framework I was really happy to
                work there.
                <br /><br />
                Threw Memucho I made my first experience with developing
                software in a company, which was great. In 2019 I quit my work
                by Memucho to switch to
                <a @click="scrollToElement('mirrads')">Mirrads</a>
              </p>
            </div>
          </div>
        </div>

        <div class="flex q-pb-lg q-mt-lg">
          <div>
            <h4 id="contact">Contact</h4>
            <a href="mailto:marco.reisinger@t-online.de"
              >marco.reisinger@t-online.de</a
            >
          </div>
          <div></div>
        </div>
      </div>
      <div class="col-2"></div>
    </div>
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { scroll } from 'quasar';
const { getScrollTarget, setVerticalScrollPosition } = scroll;
import vueBadge from '../components/vueBadge.vue';
import androidBadge from '../components/androidBadge.vue';
import XdBadge from 'src/components/xd-badge.vue';

export default defineComponent({
  name: 'PageIndex',
  components: { vueBadge, androidBadge, XdBadge },
  methods: {
    scrollToElement(id: string) {
      const el = document.getElementById(id);
      if (el) {
        const target = getScrollTarget(el);
        const offset = el.offsetTop - 50;
        const duration = 400;
        // eslint-disable-next-line @typescript-eslint/no-unsafe-argument
        setVerticalScrollPosition(target, offset, duration);
      }
    },
    getAge() {
      const birthDate = new Date('2002/05/27');
      const today = new Date();
      let age = today.getFullYear() - birthDate.getFullYear();
      const m = today.getMonth() - birthDate.getMonth();
      if (m < 0 || (m === 0 && today.getDate() < birthDate.getDate())) {
        age--;
      }
      return age;
    },
  },
});
</script>
