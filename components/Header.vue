<template>
  <div class="bg-[#1d1d1d] text-gray-100 w-full pt-[4.375rem] lg:pt-[7.5rem]">
    <Container>
      <div class="header__wrapper">
        <div class="header__content w-full lg:w-8/12 text-center lg:text-left">
          <h1 class="text-5xl lg:text-8xl font-serif mt-[1.75rem] lg:mt-none">
            Vicente Zurita
          </h1>

          <h2 class="text-2xl lg:text-3xl mt-[1.875rem] lg:mt-[2.5rem]">
            Full Stack Software Developer
          </h2>

          <a href="#contact" class="header__call-to-action">
            Let's have a chat
          </a>
        </div>

        <div class="w-full lg:w-4/12">
          <div class="header__picture">
            <nuxt-img
              sizes="sm:212px lg:350px"
              src="/images/avatars/vicentePfp.webp"
              alt="vicente-profile-picture"
              class="w-full h-full aspect-w-1 aspect-h-1"
            />
          </div>
        </div>
      </div>
    </Container>
  </div>
</template>

<script>
import Container from './Container.vue'

export default {
  name: 'Header',
  components: {
    Container,
  },
}
</script>

<style lang="postcss">
.header__wrapper {
  @apply flex flex-col-reverse lg:flex-row pb-[154px] lg:pb-[206px];
}
.header__picture {
  @apply border-gray-100 border-8 rounded-full overflow-hidden w-8/12 md:w-4/12 lg:w-full mx-auto lg:mx-[0px];
}
.header__call-to-action {
  @apply inline-block text-xl lg:text-2xl bg-gray-100 text-[#1d1d1d] py-2 lg:py-4 px-[5.625rem] lg:px-10 rounded mt-[2.5rem] hover:bg-[#28f3c3];
}
</style>
