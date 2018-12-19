<template>
    <div>
        <div class="container">
        <app-photo :style='{gridColumn: "1/5", gridRow:"1/3", position:"relative"}'>
                <p class="title">Bounce In / Bounce Out</p>
                <img src="./photos/photo01.jpg" @click="showLarge">
        </app-photo>
        <app-photo :style='{gridColumn: "5/7", gridRow:"1/2"}'>
                <img src="./photos/photo02.jpg" >
        </app-photo>
        <app-photo :style='{gridColumn: "5/7", gridRow:"2/3"}'>
                <img src="./photos/photo03.jpg" >
        </app-photo>
        <app-photo :style='{gridColumn: "1/3", gridRow:"3/4"}'>
                <img src="./photos/photo04.jpg" >
        </app-photo>
        <app-photo :style='{gridColumn: "1/3", gridRow:"4/5"}'>
                <img src="./photos/photo05.jpg" >
        </app-photo>
        <app-photo :style='{gridColumn: "3/7", gridRow:"3/5"}'>
                <img src="./photos/photo06.jpg" >
        </app-photo>
        <app-photo :style='{gridColumn: "1/3", gridRow:"5/6"}'>
                <img src="./photos/photo07.jpg" >
        </app-photo>
        <app-photo :style='{gridColumn: "3/5", gridRow:"5/6"}'>
                <img src="./photos/photo09.jpg"  >
        </app-photo>
        <app-photo :style='{gridColumn: "5/7", gridRow:"5/6"}'>
                <img src="./photos/photo08.jpg" >
        </app-photo>
         <app-photo :style='{gridColumn: "1/5", gridRow:"6/8"}'>
                <img src="./photos/photo13.jpg" >
        </app-photo>
         <app-photo :style='{gridColumn: "5/7", gridRow:"6/7"}'>
                <img src="./photos/photo11.jpg" >
        </app-photo>
         <app-photo :style='{gridColumn: "5/7", gridRow:"7/8"}'>
                <img src="./photos/photo12.jpg" >
        </app-photo>
        
    </div>
        <app-show-photo></app-show-photo>
    </div>
   
</template>

<script>
    import Photo from './components/Photo.vue';
    import ShowPhoto from './components/ShowPhoto.vue';
    

    
    export default {
        components: {
            'appPhoto' : Photo,
            'appShowPhoto' : ShowPhoto
        },
        methods: {
            showLarge(e) {
                const photo = e.target;

            }
        }
    }
</script>

<style>
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
        left:35%;
        color:#ffff;
        text-transform: uppercase;
        font-weight: bold;
        font-size: 20px;
    }
    .largePhoto {
        
    }
   
</style>