<template>
    <div>
        <div class="container"> 
            <div v-for='el in position' >
                <app-photo :style="{{el}}">
            </app-photo>
            </div>
            
            <!--<app-photo :style='position[0]' >
                <img src="./photos/photo01.jpg" @mouseover="showText" @mouseleave="showText">
                <app-photo-title>
                    <h1  class="title" v-if="activeText">Bounce In Down</h1>
                </app-photo-title>
            </app-photo>
            <app-photo :style='position[1]'>
                    <img src="./photos/photo02.jpg">
            </app-photo>
            <app-photo :style='position[2]'>
                    <img src="./photos/photo03.jpg">
            </app-photo>
            <app-photo :style='{gridColumn: "1/3", gridRow:"3/4"}'>
                    <img src="./photos/photo04.jpg">
            </app-photo>
            <app-photo :style='{gridColumn: "1/3", gridRow:"4/5"}'> 
                    <img src="./photos/photo05.jpg">
            </app-photo>
            <app-photo :style='{gridColumn: "3/7", gridRow:"3/5"}'>
                    <img src="./photos/photo06.jpg">
            </app-photo>
            <app-photo :style='{gridColumn: "1/3", gridRow:"5/6"}'>
                    <img src="./photos/photo07.jpg">
            </app-photo>
            <app-photo :style='{gridColumn: "3/5", gridRow:"5/6"}'>
                    <img src="./photos/photo09.jpg">
            </app-photo>
            <app-photo :style='{gridColumn: "5/7", gridRow:"5/6"}'>
                    <img src="./photos/photo08.jpg">
            </app-photo>
             <app-photo :style='{gridColumn: "1/5", gridRow:"6/8"}'>
                    <img src="./photos/photo13.jpg">
            </app-photo>
             <app-photo :style='{gridColumn: "5/7", gridRow:"6/7"}'>
                    <img src="./photos/photo11.jpg">
            </app-photo>
             <app-photo :style='{gridColumn: "5/7", gridRow:"7/8"}'>
                    <img src="./photos/photo12.jpg">
            </app-photo>-->
        </div>
        <app-show-photo></app-show-photo>
    </div>
   
</template>

<script>
    import Photo from './components/Photo.vue';
    import ShowPhoto from './components/ShowPhoto.vue';
    import PhotoTitle from './components/PhotoTitle.vue';
    import {showPhotoBus} from './main.js';
    
    export default {
        data() {
            return {
                activeText:false,
                position: [
                    'gridColumn: "1/5",gridRow:"1/3"',
                    'gridColumn: "5/7", gridRow:"1/2"',
                    'gridColumn: "5/7", gridRow:"2/3"'
                    
                ],
                photos: [
                    {position:'{gridColumn: "1/5", gridRow:"1/3"}', source: "./photos/photo01.jpg", title: 'Bounce In Down'}
                    
                ]
            }
        },
        methods: {
            showText() {
                this.activeText=!this.activeText;
            }
        },
        components: {
            'appPhoto' : Photo,
            'appShowPhoto' : ShowPhoto,
            'appPhotoTitle' : PhotoTitle
        }

    }
</script>

<style>
    .position {
        grid-column: "1/5";
        grid-row:"1/3";
    }
    .container {
        width:80%;
        margin: 40px auto;
        display: grid;
        grid-template-columns: 16% 16% 16% 16% 16% 16%;
        grid-template-rows: 14% 14% 14% 14% 14% 14% 14%;
        grid-gap:3px;
        position: relative;
    }
    .title {
        z-index:50;
        position:absolute;
        top:40%;
        left:30%;
        color:#ffff;
        text-transform: uppercase;
        font-weight: bold;
        font-family: 'Verdana';
    }

    

   
</style>