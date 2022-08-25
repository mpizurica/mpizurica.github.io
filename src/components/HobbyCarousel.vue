<template>
    <div class="container">
        <input type="radio" name="slider" id="item-1">
        <input type="radio" name="slider" id="item-2" checked>
        <input type="radio" name="slider" id="item-3">
        <input type="radio" name="slider" id="item-4">
        <input type="radio" name="slider" id="item-5">
        <div class="cards">
            <label class="card" for="item-1" id="card-1">
                <img src="../assets/marija_cropped.jpeg" alt="">
            </label>
            <label class="card" for="item-2" id="card-2">
                <img src="../assets/marija_cropped.jpeg" alt="">
            </label>
            <label class="card" for="item-3" id="card-3">
                <img src="../assets/marija_cropped.jpeg" alt="">
            </label>
            <label class="card" for="item-4" id="card-4">
                <img src="../assets/marija_cropped.jpeg" alt="">
            </label>
            <label class="card" for="item-5" id="card-5">
                <img src="../assets/marija_cropped.jpeg" alt="">
            </label>
        </div>
    </div>
</template>

<style scoped>
img {
    @apply rounded-xl;
    @apply object-cover;
    @apply shadow-xl
}

input[type=radio] {
  display: none;
}

.card {
  position: absolute;
  width: 33%;
  height: 100%;
  left: 0;
  right: 0;
  margin: auto;
  transition: transform .4s ease;
  cursor: pointer;
}

.container {
  width: 100%;
  max-width: 800px;
  max-height: 600px;
  height: 100%;
  transform-style: preserve-3d;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.cards {
  position: relative;
  width: 100%;
  height: 100%;
  margin-bottom: 20px;
}

/* cards one before */
#item-1:checked ~ .cards #card-5, #item-2:checked ~ .cards #card-1, #item-3:checked ~ .cards #card-2, #item-4:checked ~ .cards #card-3, #item-5:checked ~ .cards #card-4 {
  transform-origin: center center; 
  transform: translate(-60%, -60%) scale(.8);
  /* opacity: .4; */
  z-index: 0;
}

/* cards two before */
#item-1:checked ~ .cards #card-4, #item-2:checked ~ .cards #card-5, #item-3:checked ~ .cards #card-1, #item-4:checked ~ .cards #card-2, #item-5:checked ~ .cards #card-3 {
  transform: translatex(-100%) scale(.6);
  /* opacity: .4; */
  z-index: -1;
}

/* card one after */
#item-1:checked ~ .cards #card-2, #item-2:checked ~ .cards #card-3, #item-3:checked ~ .cards #card-4, #item-4:checked ~ .cards #card-5, #item-5:checked ~ .cards #card-1 {
  transform: translatex(60%) scale(.8);
  /* opacity: .4; */
  z-index: 0;
}

/* card two after */
#item-1:checked ~ .cards #card-3, #item-2:checked ~ .cards #card-4, #item-3:checked ~ .cards #card-5, #item-4:checked ~ .cards #card-1, #item-5:checked ~ .cards #card-2 {
  transform: translatex(100%) scale(.6);
  /* opacity: .4; */
  z-index: -1;
}

/* card selected */
#item-1:checked ~ .cards #card-1, #item-2:checked ~ .cards #card-2, #item-3:checked ~ .cards #card-3, #item-4:checked ~ .cards #card-4, #item-5:checked ~ .cards #card-5 {
  transform: translatex(0) scale(1);
  /* opacity: 1; */
  z-index: 1;
  
}
</style>