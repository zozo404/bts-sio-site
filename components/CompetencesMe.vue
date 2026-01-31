<template>
  <!-- my skills, we display technology logos with a "v-for" and an import from Sanity -->
  <div class="pb-5 fade-scroll" :class="{ visible: isVisible }">
    <p class="text-center pb-3 text-lg">
      Voici toutes les technologies avec lesquelles j'ai pu travailler
    </p>
    <div class="flex justify-center flex-wrap gap-8 items-center px-1">
      <div v-for="skill in skills" :key="skill._id" class="flex items-center flex-col self-end">
        <nuxt-img
          provider="sanity"
          :src="skill.imageUrl.asset._ref"
          placeholder
          class="w-16 h-auto"
          :alt="skill.name"
        />
        <p class="mt-3 first-letter:uppercase">{{ skill.name }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import scrollFadeMixin from '~/mixins/scrollFadeMixin'

export default {
  name: 'CompetencesMe',
  mixins: [scrollFadeMixin],
  props: {
    skills: {
      default: null,
      type: Array
    }
  }
}
</script>
