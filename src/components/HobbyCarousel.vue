<template>
  <div class="container">
    <input type="radio" name="slider" id="item-1">
    <input type="radio" name="slider" id="item-2">
    <input type="radio" name="slider" id="item-3" checked>
    <input type="radio" name="slider" id="item-4">
    <input type="radio" name="slider" id="item-5">
    <!-- Display overlay if checked or on hover ? -->
    <!-- Turn overlayed picture into a subcomponent. -->
    <div class="cards mx-auto">
      <label class="card" for="item-1" id="card-1">
        <div class="w-full h-full">
          <img src="../assets/travel/capitol_reef.jpeg" alt="">
          <div class="rounded-xl absolute top-0 left-0 w-full h-full opacity-40 bg-gradient-to-b from-stone-800">
          </div>
          <div class="rounded-xl absolute top-0 left-0 w-full h-full p-5">
            <h1 class="text-white font-bold opacity-100">Capitol Reef National Park</h1>
            <h2 class="text-white opacity-100">Utah, U.S.A.</h2>
          </div>
        </div>
      </label>
      <label class="card" for="item-2" id="card-2">
        <div class="w-full h-full">
          <img src="../assets/travel/henry_coe.jpeg" alt="">
          <div class="rounded-xl absolute top-0 left-0 w-full h-full opacity-40 bg-gradient-to-b from-stone-800">
          </div>
          <div class="rounded-xl absolute top-0 left-0 w-full h-full p-5">
            <h1 class="text-white font-bold opacity-100">Henry W. Coe State Park</h1>
            <h2 class="text-white opacity-100">California, U.S.A.</h2>
          </div>
        </div>
      </label>
      <label class="card" for="item-3" id="card-3">
        <div class="w-full h-full">
          <img src="../assets/travel/monterey_aquarium.jpeg" alt="">
          <div class="rounded-xl absolute top-0 left-0 w-full h-full opacity-40 bg-gradient-to-b from-stone-800">
          </div>
          <div class="rounded-xl absolute top-0 left-0 w-full h-full p-5">
            <h1 class="text-white font-bold opacity-100">Monterey Aquarium</h1>
            <h2 class="text-white opacity-100">California, U.S.A.</h2>
          </div>
        </div>
      </label>
      <label class="card" for="item-4" id="card-4">
        <div class="w-full h-full">
          <img src="../assets/travel/monument_valley.jpeg" alt="">
          <div class="rounded-xl absolute top-0 left-0 w-full h-full opacity-40 bg-gradient-to-b from-stone-800">
          </div>
          <div class="rounded-xl absolute top-0 left-0 w-full h-full p-5">
            <h1 class="text-white font-bold opacity-100">Monument Valley</h1>
            <h2 class="text-white opacity-100">Arizona, U.S.A.</h2>
          </div>
        </div>
      </label>
      <label class="card" for="item-5" id="card-5">
        <div class="w-full h-full">
          <img src="../assets/travel/nyc.jpeg" alt="">
          <div class="rounded-xl absolute top-0 left-0 w-full h-full opacity-40 bg-gradient-to-b from-stone-800">
          </div>
          <div class="rounded-xl absolute top-0 left-0 w-full h-full p-5">
            <h1 class="text-white font-bold opacity-100">New York City</h1>
            <h2 class="text-white opacity-100">New York, U.S.A.</h2>
          </div>
        </div>
      </label>
    </div>
  </div>
</template>

<style scoped>
label {
  @apply w-1/2;
  @apply h-80;
}

img {
  @apply w-full;
  @apply h-full;
  @apply rounded-xl;
  @apply object-cover;
  @apply shadow-xl;
  /* @apply w-full; */
  /* @apply h-full; */
  /* @apply h-80; */
  /* @apply w-80; */
}

input[type=radio] {
  display: none;
}

.card {
  position: absolute;
  left: 0;
  right: 0;
  margin: auto;
  transition: transform .5s ease;
  cursor: pointer;
}

.container {
  width: 100%;
  max-width: 100%;
  height: 100%;
  transform-style: preserve-3d;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.cards {
  /* padding-top: 200px; */
  /* margin-top: -200px; */
  /* margin-bottom: 20px; */
}

/* cards one before */
#item-1:checked~.cards #card-5,
#item-2:checked~.cards #card-1,
#item-3:checked~.cards #card-2,
#item-4:checked~.cards #card-3,
#item-5:checked~.cards #card-4 {
  transform: translatex(-45%) scale(.8);
  /* transition-delay: 250ms; */
  z-index: 0;
}

/* cards two before */
#item-1:checked~.cards #card-4,
#item-2:checked~.cards #card-5,
#item-3:checked~.cards #card-1,
#item-4:checked~.cards #card-2,
#item-5:checked~.cards #card-3 {
  transform: translatex(-80%) scale(.6);
  /* transition-delay: 500ms; */
  z-index: -2;
}

/* card one after */
#item-1:checked~.cards #card-2,
#item-2:checked~.cards #card-3,
#item-3:checked~.cards #card-4,
#item-4:checked~.cards #card-5,
#item-5:checked~.cards #card-1 {
  transform: translatex(45%) scale(.8);
  /* transition-delay: 250ms; */
  z-index: 1;
}

/* card two after */
#item-1:checked~.cards #card-3,
#item-2:checked~.cards #card-4,
#item-3:checked~.cards #card-5,
#item-4:checked~.cards #card-1,
#item-5:checked~.cards #card-2 {
  transform: translatex(80%) scale(.6);
  /* transition-delay: 500ms; */
  z-index: -1;
}

/* card selected */
#item-1:checked~.cards #card-1,
#item-2:checked~.cards #card-2,
#item-3:checked~.cards #card-3,
#item-4:checked~.cards #card-4,
#item-5:checked~.cards #card-5 {
  transform: translatex(0) scale(1);
  /* transition-delay: 250ms; */
  z-index: 2;

}

@keyframes centerMoveLeft {
  from {
    transform: translatex(0) scale(1);
    z-index: 2;
  }

  to {
    transform: translatex(-45%) scale(.8);
    z-index: 0;
  }
}
</style>