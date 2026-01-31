<template>
  <div class="fade-scroll" :class="{ visible: isVisible }">
    <div class="flex flex-col items-center mt-7">
      <p class="text-center mt-2 w-1/2 text-lg pb-4 font-comfortaa">
        <br>
        La veille technologique consiste à s'informer en continu sur les
        dernières innovations, les failles de sécurité et les évolutions des
        outils informatiques. Dans un secteur qui évolue quotidiennement, elle
        est indispensable pour rester compétitif et garantir la sécurité des
        infrastructures.
        <br>
        <br>
        Les deux types de veille :
        <ul class="list-disc">
          <li>
            La Veille Passive (Push) : On reçoit l'information sans effort particulier via des flux RSS, des newsletters ou des alertes Google. L'information vient à nous.
          </li>
          <p>
            Comme avec newsletters quotidiennes que je reçois de
            <a class="text-orange-400" href="https://www.xmco.fr/yuno-veille-vulnerabilites-cybersecurite/" target="_blank">
              Yuno by XMCO
            </a>
          </p>
          <br>
          <li>
            La Veille Active (Pull) : On recherche activement des informations précises sur des forums spécialisés, de la documentation technique. On va chercher l'information.
          </li>
          <p>
            Via des youtubeurs comme
            <a class="text-orange-400" href="https://www.youtube.com/@LeoTechMaker/videos" target="_blank">Léo - TechMaker</a>
            <span>
              ou aussi
            </span>
            <a class="text-orange-400" href="https://www.it-connect.fr/actualites/" target="_blank">IT Connect</a>
          </p>
        </ul>
      </p>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import scrollFadeMixin from '~/mixins/scrollFadeMixin'

export default {
  mixins: [scrollFadeMixin],
  computed: {
    ...mapGetters(['getPages'])
  }
}
</script>

<style>
</style>
