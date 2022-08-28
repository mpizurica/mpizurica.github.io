<template>
    <!-- always visible  -->
    <div class="flex flex-col space-y-2">
        <div class="grid grid-cols-5">
            <div class="">
                <p class="list-info">Nov `22</p>
            </div>
            <div class="col-span-4">
                <p>Paper accepted at conference!</p>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class="">
                <p class="list-info">Mar `22</p>
            </div>
            <div class="col-span-4">
                <p>Gave a talk, check out the slides.</p>
            </div>
        </div>
    </div>
    <!-- expand section -->
    <div v-show="expanded" class="flex flex-col space-y-2 pt-2">
        <div class="grid grid-cols-5">
            <div class="">
                <p class="list-info">Nov `22</p>
            </div>
            <div class="col-span-4">
                <p>Paper accepted at conference!</p>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class="">
                <p class="list-info">Mar `22</p>
            </div>
            <div class="col-span-4">
                <p>Gave a talk, check out the slides.</p>
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