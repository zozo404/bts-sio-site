<template>
  <div>
    <div class="flex flex-col items-center">
      <p class="text-center mt-6 w-1/2 text-lg pb-4 font-comfortaa">
        Le groupe<span
          class="text-amber-400"
        >
          Elsan
        </span>
        est leader de l'hospitalisation privée en France, il joue un rôle majeur dans le secteur de la santé. Implanté sur l’ensemble du territoire, il allie proximité et excellence médicale pour offrir des soins de qualité au plus grand nombre..
      </p>
    </div>
    <!-- elsan imported from Sanity -->
    <div class="flex justify-center lg:col-span-1 lg:h-full h-2/3">
      <span class="sr-only">Elsan</span>
      <nuxt-img
        provider="sanity"
        :src="Logo.imageId.asset._ref"
        :alt="Logo.imageId.alt"
        class="h-auto lg:h-96 rounded-lg"
      />
    </div>
  </div>
</template>
<script>
import { mapGetters } from 'vuex'
export default {
  name: 'LogoApp',
  computed: {
    ...mapGetters(['getPages']),
    Logo () {
      return this.getPages.find(el => el.name === 'Elsan')
    }
  }
}
</script>
