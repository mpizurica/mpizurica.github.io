<template>
    <div class="slider-container">
        <input type="radio" name="slider2" id="slider-item-1">
        <input type="radio" name="slider2" id="slider-item-2" checked>
        <input type="radio" name="slider2" id="slider-item-3">
        <input type="radio" name="slider2" id="slider-item-4">
        <input type="radio" name="slider2" id="slider-item-5">
        <div class="card-container flex w-full h-full space-x-2">
            <div class="overlay-container" id="overlay-container-1">
                <label id="slider-card-1" for="slider-item-1">
                    <div class="w-full h-full relative">
                        <img src="../assets/travel/capitol_reef.jpeg" class="" alt="">
                        <div class="overlay">
                            <div
                                class="rounded-xl absolute top-0 left-0 w-full h-full opacity-40 bg-gradient-to-b from-stone-800">
                            </div>
                            <div class="rounded-xl absolute top-0 left-0 w-full h-full p-5">
                                <h1 class="text-white font-bold opacity-100">Capitol Reef <br class="block sm:hidden"/> National Park</h1>
                                <h2 class="text-white opacity-100">Utah, U.S.A.</h2>
                            </div>
                        </div>
                    </div>
                </label>
            </div>
            <div class="overlay-container" id="overlay-container-2">
                <label id="slider-card-2" for="slider-item-2">
                    <div class="w-full h-full relative">
                        <img src="../assets/travel/monterey_aquarium.jpeg" class="" alt="">
                        <div class="overlay">
                            <div
                                class="rounded-xl absolute top-0 left-0 w-full h-full opacity-40 bg-gradient-to-b from-stone-800">
                            </div>
                            <div class="rounded-xl absolute top-0 left-0 w-full h-full p-5">
                                <h1 class="text-white font-bold opacity-100">Monterey Aquarium</h1>
                                <h2 class="text-white opacity-100">California, U.S.A.</h2>
                            </div>
                        </div>
                    </div>
                </label>
            </div>
            <div class="overlay-container" id="overlay-container-3">
                <label id="slider-card-3" for="slider-item-3">
                    <div class="w-full h-full relative">
                        <img src="../assets/travel/monument_valley.jpeg" class="" alt="">
                        <div class="overlay">
                            <div
                                class="rounded-xl absolute top-0 left-0 w-full h-full opacity-40 bg-gradient-to-b from-stone-800">
                            </div>
                            <div class="rounded-xl absolute top-0 left-0 w-full h-full p-5">
                                <h1 class="text-white font-bold opacity-100">Monument Valley</h1>
                                <h2 class="text-white opacity-100">Arizona, U.S.A.</h2>
                            </div>
                        </div>
                    </div>
                </label>
            </div>
            <div class="overlay-container" id="overlay-container-4">
                <label id="slider-card-4" for="slider-item-4">
                    <div class="w-full h-full relative">
                        <img src="../assets/travel/nyc.jpeg" class="" alt="">
                        <div class="overlay">
                            <div
                                class="rounded-xl absolute top-0 left-0 w-full h-full opacity-40 bg-gradient-to-b from-stone-800">
                            </div>
                            <div class="rounded-xl absolute top-0 left-0 w-full h-full p-5">
                                <h1 class="text-white font-bold opacity-100">New York City</h1>
                                <h2 class="text-white opacity-100">New York, U.S.A.</h2>
                            </div>
                        </div>
                    </div>
                </label>
            </div>
            <div class="overlay-container" id="overlay-container-5">
                <label id="slider-card-5" for="slider-item-5">
                    <div class="w-full h-full relative">
                        <img src="../assets/travel/henry_coe.jpeg" class="" alt="">
                        <div class="overlay">
                            <div
                                class="rounded-xl absolute top-0 left-0 w-full h-full opacity-40 bg-gradient-to-b from-stone-800">
                            </div>
                            <div class="rounded-xl absolute top-0 left-0 w-full h-full p-5">
                                <h1 class="text-white font-bold opacity-100">Henry W. Coe <br class="block sm:hidden"/>State Park</h1>
                                <h2 class="text-white opacity-100">California, U.S.A.</h2>
                            </div>
                        </div>
                    </div>
                </label>
            </div>
        </div>
    </div>

</template>

<style scoped>
img {
    @apply h-full;
    @apply w-full;
    @apply object-cover;
    @apply rounded-xl;
    @apply shadow-xl;
}

input[type=radio] {
    display: none;
}

.slider-container {
    height: 40vh;
}
@screen md {
    .slider-container {
        height: 40vh;
    }
}
@screen xl {
    .slider-container {
        height: 60vh;
    }
}

.overlay-container {
    @apply h-full;
    transition: width 1s ease;
}

.overlay {
    transition: opacity 1s ease 500ms;
    white-space: nowrap;
}
.overlay-container {
    @apply w-12;
}

.overlay {
    @apply opacity-0;
}

#slider-item-1:checked~.card-container #overlay-container-1 .overlay {
    @apply opacity-100
}
#slider-item-2:checked~.card-container #overlay-container-2 .overlay {
    @apply opacity-100
}
#slider-item-3:checked~.card-container #overlay-container-3 .overlay {
    @apply opacity-100
}
#slider-item-4:checked~.card-container #overlay-container-4 .overlay {
    @apply opacity-100
}
#slider-item-5:checked~.card-container #overlay-container-5 .overlay {
    @apply opacity-100
}
#slider-item-1:checked~.card-container #overlay-container-1 {
    @apply w-full;
}

#slider-item-2:checked~.card-container #overlay-container-2 {
    @apply w-full;
}

#slider-item-3:checked~.card-container #overlay-container-3 {
    @apply w-full;
}

#slider-item-4:checked~.card-container #overlay-container-4 {
    @apply w-full;
}

#slider-item-5:checked~.card-container #overlay-container-5 {
    @apply w-full;
}
</style>