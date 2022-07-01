<template>
  <Container>
    <div class="text-left md:ml-1 mt-[50px]">
      <h2 class="font-serif text-[#1d1d1d] text-4xl md:text-5xl">
        Projects
      </h2>

      <div class="passion-PassionProjects__cards">
        <ProjectCard
          v-for="project in PassionProjects"
          :key="project.idx"
          :title="project.title"
          :categories="project.categories"
          :excerpt="project.excerpt"
          :image="project.image"
          :type="project.type"
        />
      </div>
    </div>
  </Container>
</template>

<script>
import Container from '@/components/Container.vue'
import ProjectCard from '@/components/ProjectCard.vue'

export default {
  name: 'PassionProjects',
  components: {
    Container,
    ProjectCard,
  },
  data() {
    return {
      PassionProjects: [
        {
          title: 'Ipeheme Webpage',
          categories: ['Django', 'Bootstrap5','PostgreSQL','Linux'],
          excerpt: 'Video display website for videographer Ipeheme can display youtube or vimeo videos.',
          image: {
            src: '/images/Ipeheme.webp',
            alt: "Screenshot Webpage",
          },
          type: 'Full Stack',
        },
        {
          title: 'My Own Portfolio',
          categories: ['Vue.js', 'Tailwind.css', 'NuxtJs'],
          excerpt: 'Website for displaying my own portfolio, it was done for learning and work purposes on a language i did not know.',
          image: {
            src: '/images/VicenteFolio.webp',
            alt: 'Screenshot of this webpage',
          },
          type: 'Full Stack',
        },
        {
          title: 'Art Chili',
          categories: ['Wordpress'],
          excerpt: 'Content update and management website for art firm.',
          image: {
            src: '/images/artChili.webp',
            alt: 'ScreenShot ArtChili',
          },
          type: 'FrontEnd',
        },
        {
          title: 'Paloma Site',
          categories: ['ToDecide'],
          excerpt: 'Portfolio site for event producer',
          image: {
            src: '/images/Sports_Bet.webp',
            alt: "Woman's hands knitting",
          },
          type: 'Full Stack',
        },
      ],
    }
  },
}
</script>

<style lang="postcss">
.passion-PassionProjects__cards {
  @apply lg:mt-[10px] grid grid-cols-1 lg:grid-cols-2 lg:gap-[20px] pb-[60px];
}
</style>
