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
</script>

<template>
  <!-- main container -->
  <div class="xl:w-3/5 md:w-4/5 w-5/5 bg-gray-50 rounded-xl mx-5 md:mx-auto my-10 md:px-20 px-10 pb-10">
    <!-- heading  -->
    <div class="flex flex-col text-center pt-10">
      <MainHeader class="mb-5"/>
      <MainInfo />
    </div>

    <hr class="mt-10">
    <!-- header with link -->
    <div class="py-10">
      <header class="flex justify-between lg:w-1/2 md:w-3/4 mx-auto">
        <LayoutHeaderButton text="about" />
        <LayoutHeaderButton text="news" />
        <LayoutHeaderButton text="publications" />
        <LayoutHeaderButton text="hobbies" />
      </header>
    </div>
    <!-- main section -->
    <div class="md:grid md:grid-cols-2 md:space-x-8 flex flex-col">
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
    <div>
      <SectionHeader text="News" />
      <NewsList />
    </div>
    <!-- publication section -->
    <hr class="my-10">
    <div>
      <SectionHeader text="Publications" />
      <!-- publications -->
      <PublicationList />
    </div>
    <!-- footer  -->
    <hr class="my-10">
    <LayoutFooter />
  </div>
</template>


<style scoped>
</style>
