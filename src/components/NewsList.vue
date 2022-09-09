<template>
    <!-- always visible  -->
    <div class="flex flex-col space-y-2">
        <div class="grid grid-cols-5">
            <div class="">
                <p class="list-info">Aug `22</p>
            </div>
            <div class="col-span-4">
                <p>Got prize for best master thesis of the Faculty of Engineering and Architecture at Ghent Univerisity for my work ""!</p>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class="">
                <p class="list-info">Jul `22</p>
            </div>
            <div class="col-span-4">
                <p>Our paper "Self-supervised Multimodal Pre-training for Lung Adenocarcinoma overall Survival Prediction" was accepted at the 23rd International Conference on Bioinformatics and Computational Biology, in Las Vegas (USA)!</p>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class="">
                <p class="list-info">Mar `22</p>
            </div>
            <div class="col-span-4">
                <p>Gave a talk at the Applied Bioinformatics in Life Sciences Conference in Leuven (Belgium)!</p>
            </div>
        </div>
    </div>
    <!-- expand section -->
    <div v-show="expanded" class="flex flex-col space-y-2 pt-2">
        <div class="grid grid-cols-5">
            <div class="">
                <p class="list-info">Nov `21</p>
            </div>
            <div class="col-span-4">
                <p>Started my 1y research stay at Stanford University!</p>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class="">
                <p class="list-info">Apr `21</p>
            </div>
            <div class="col-span-4">
                <p>Received a scholarship from the Belgian American Education Foundation.</p>
            </div>
        </div>
    </div>
    <div class="pt-2 link">
        <button v-on:click="expanded = !expanded">
            <p>
                Click for {{expanded? 'less' : 'more'}} news.
            </p>
        </button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            expanded: false
        }
    }
}</script>
