<template>
  <q-page>
    <div id="home" class="flex headline-container row">
      <div class="col-2"></div>
      <div class="col-10 flex" style="flex-wrap: nowrap">
        <div>
          <h1 class="text-h2 text-bold">Marco Reisinger</h1>
          <h2 class="text-h5">UX Design | Software Development</h2>
        </div>
        <div style="width: 900px">
          <q-img src="/bildPortfolio.png"></q-img>
        </div>
      </div>
    </div>

    <div class="row shadow-2 sticky q-py-sm full-width bg-white">
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
      <div class="col-3"></div>
      <div class="col-6">
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

          <div class="text-h5">Mirrads</div>
          <div class="flex">
            <p>
              Mirrads is a startup from Ingolstadt which sells smart mirros.
            </p>
            <p>
              I am working for Mirrads since January 2019. <br />
              The company sells mirrors which can show digital messages, mostly
              for digital signage reasons. <br />
              To display the videos & images on the mirror we used a android tv
              box and developed our own software.<br />
              I created the whole app by myself for almost one year. <br />
              We also implemented features like face recognition, nfc, barcode
              scanners and p2p connections between the mirrors.<br />
              To control the mirrors, we needed to create our own content
              management system (CMS)<br />
              In 2021 I quit my android development and switched to the frontend
              work for the CMS.<br />
            </p>
            <p>
              I learned the most important skills at Mirrads, like building a
              proper architecture, working in a team and managing tasks
            </p>
            <div></div>
          </div>

          <div class="text-h5">GrandEvent</div>
          <div class="flex">
            <p>A university project</p>
            <div></div>
          </div>

          <div class="text-h5">Memodia</div>
          <div class="flex">
            <p>Side project by myself</p>
            <div></div>
          </div>

          <div class="text-h5">Tourgether</div>
          <div class="flex">
            <p>Another university project</p>
            <div></div>
          </div>

          <div class="text-h5">Roundtrips4you</div>
          <div class="flex">
            <p>A very big travel project, which I developed by myself.</p>
            <div></div>
          </div>

          <div class="text-h5">Memucho</div>
          <div class="flex">
            <p>The first company where I developed Sofware.</p>
            <div></div>
          </div>
        </div>

        <div class="flex q-pb-lg">
          <div>
            <h4 id="contact">Contact</h4>
            <a href="mailto:marco.reisinger@t-online.de"
              >marco.reisinger@t-online.de</a
            >
          </div>
          <div></div>
        </div>
      </div>
      <div class="col-3"></div>
    </div>
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { scroll } from 'quasar';
const { getScrollTarget, setVerticalScrollPosition } = scroll;

export default defineComponent({
  name: 'PageIndex',
  components: {},
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
