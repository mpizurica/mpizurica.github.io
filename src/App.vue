<script setup>
import MainHeader from './components/MainHeader.vue';
import LayoutHeaderButton from './components/LayoutHeaderButton.vue';
import MainText from './components/MainText.vue';
import MainPicture from './components/MainPicture.vue';
import MainButton from './components/MainButton.vue';
import SectionHeader from './components/SectionHeader.vue';
import NewsList from './components/NewsList.vue';
import MainInfo from './components/MainInfo.vue';
import PublicationList from './components/PublicationList.vue';
import LayoutFooter from './components/LayoutFooter.vue';
import HobbyCarousel from './components/HobbyCarousel.vue';
</script>

<template>
  <!-- main container -->
  <div id="about" class="xl:w-3/5 md:w-4/5 w-5/5 mx-5 md:mx-auto pt-10 ">
    <!-- heading  -->
    <div class="flex flex-col text-center pb-5">
      <MainHeader class="mb-5" />
      <MainInfo />
    </div>
  </div>

  <!-- header with link -->
  <div id="sticky-header" class="py-5 sticky top-0 z-50 bg-gray-50 duration-200"
    :class="{ scrolled: !view.atTopOfPage }">
    <div class="xl:w-3/5 md:w-4/5 w-5/5 mx-5 md:mx-auto">
      <header class=" flex justify-between md:space-x-8">
        <hr class="w-full my-auto hidden md:block" />
        <LayoutHeaderButton text="about" link="#about" />
        <LayoutHeaderButton text="news" link="#news" />
        <LayoutHeaderButton text="publications" link="#publications" />
        <LayoutHeaderButton text="hobbies" link="#hobbies" />
        <hr class="w-full my-auto hidden md:block" />
      </header>
    </div>
  </div>
  <div class="xl:w-3/5 md:w-4/5 w-5/5 mx-5 md:mx-auto pb-10 ">
    <!-- main section -->
    <div class="md:grid md:grid-cols-2 md:space-x-8 flex flex-col pt-5">
      <!-- logo, text and button  -->
      <div class="justify-between flex flex-col md:order-1 order-2">
        <MainText />
        <MainButton class="mt-10" />
      </div>
      <!-- picture  -->
      <div class="md:order-2 order-1">
        <MainPicture class="mb-5 md:mb-0" />
      </div>
    </div>
    <!-- news section -->
    <hr class="my-10">
    <div id="news" >
      <SectionHeader text="News" />
      <NewsList />
    </div>
    <!-- publication section -->
    <hr class="my-10">
    <div id="publications">
      <SectionHeader text="Publications" />
      <!-- publications -->
      <PublicationList />
    </div>
    <!-- hobby section -->
    <hr class="my-10">
    <div id="hobbies">
      <SectionHeader text="Hobbies" />
      <!-- hobbies -->
      <h3 class="text-lg font-semibold">Photography & Travel</h3>
      <HobbyCarousel class="h-52 pb-52"/>
      <h3 class="text-lg font-semibold">Artwork</h3>
      <!-- <HobbyCarousel class="h-52 pb-52"/> -->
      <h3 class="text-lg font-semibold">Reading</h3>
      <!-- <HobbyCarousel class="h-52 pb-52"/> -->
    </div>
    <!-- footer  -->
    <hr class="my-10">
    <LayoutFooter />
  </div>
</template>

<script>
export default {
  data() {
    return {
      view: {
        atTopOfPage: true,
      },
    };
  },
  // a beforeMount call to add a listener to the window
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  methods: {
    // the function to call when the user scrolls, added as a method
    handleScroll() {
      // get position of sticky header
      var stickyHeader = document.getElementById('sticky-header')
      if (stickyHeader.getBoundingClientRect().y == 0) {
        // user is scrolled
        if (this.view.atTopOfPage) {
          this.view.atTopOfPage = false;
        }
      } else {
        // user is at top of page
        if (!this.view.atTopOfPage) this.view.atTopOfPage = true;
      }
    },
  },
};
</script>

<style>
.scrolled {
  @apply shadow-lg;
}

html {
  scroll-behavior: smooth;
}

:target:before {
  content: "";
  display: block;
  height: 100px;
  margin: -100px 0 0;
  /* display: block;
  position: relative;
  top: -100px;
  visibility: hidden; */
}
</style>