<template>
  <div class="fade-scroll" :class="{ visible: isVisible }">
    <!-- displays a photo of me that is imported by adding a description and the buttons to their respective link -->
    <div class="flex flex-col items-center">
      <Logo />
      <p class="text-center mt-2 w-1/2 text-lg pb-4 font-comfortaa">
        👋, Je suis Enzo 👨‍💻. Jonglant entre le dev web et le réseau,<span
          class="text-orange-500"
        >
          je suis actuellement en alternance au sein du groupe Elsan
        </span>
        pour mon BTS SIO SISR afin de me spécialiser en réseau. Je souhaite mettre mon expertise au service du
        groupe à la fin de mes études.
      </p>
    </div>
    <div class="flex flex-col items-center gap-5 lg:flex-row lg:justify-center">
      <!-- to display the buttons without repeating too much, we declare a loop with a "v-for", in which we bind the data that is in the script -->
      <a
        v-for="btn in button.link"
        :key="btn.name"
        :href="btn.href"
        target="_blank"
        rel="noopener"
        class="duration-150 border-2 border-orange-400 border-opacity-50 hover:border-2 hover:border-opacity-100 rounded-full py-3 px-5"
      >{{ btn.name }}</a>
    </div>
    <Elsan />
    <div class="flex flex-col items-center mt-7">
      <p class="text-center mt-2 w-1/2 text-lg pb-4 font-comfortaa">
        <br>
        Le BTS SIO (Services Informatiques aux Organisations) forme
        en deux ans des experts en informatique capables de répondre aux besoins
        de transformation numérique des entreprises.
        <br>
        <br>
        Il propose deux spécialisations : SISR (Infrastructure, Systèmes et Réseaux) et SLAM
        (Solutions Logicielles et Applications Métiers).
      </p>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import scrollFadeMixin from '~/mixins/scrollFadeMixin'

export default {
  mixins: [scrollFadeMixin],
  data () {
    return {
      button: {
        link: [
          {
            name: 'Télécharger CV',
            href: '/CV-CUNY-Enzo–BTS-SIO-SISR.pdf'
          },
          {
            name: 'Mon Github',
            href: 'https://github.com/zozo404'
          },
          {
            name: 'Mon LinkedIn',
            href: 'https://www.linkedin.com/in/enzo-cuny/'
          },
          {
            name: 'Tableau de synthèse E5',
            href: '/BTS_SIO_Annexe_VI.5_EpreuveE5-Tableau-de-synthese_2026.xlsx'
          }
        ]
      }
    }
  },
  computed: {
    ...mapGetters(['getPages'])
  }
}
</script>

<style>
</style>
