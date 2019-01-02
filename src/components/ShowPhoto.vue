<template> 
        <transition
                enter-active-class="animated bounceInDown"
                leave-active-class="animated bounceOutDown">
                <div class="show" v-if='isShow'>
                    <img src="./../photos/photo01.jpg" class="showPhoto">
                    <button class="closeBtn" @click="showPhoto">X</button>
                </div>
            
        </transition>
</template>

<script>
    import {showPhotoBus} from './../main.js';
    export default {
        /*props: {
            isShow: {
                type: Boolean,
                deafult:false
            }
        },
        methods: {
            showPhoto() {
                this.isShow=!this.isShow;
                showPhotoBus.$emit('showingPhoto', this.isShow);
            }
        }*.
        /*props: {
            isShow: Boolean
        }*/
        data() {
            return {
                isShow:false
            };
        },
        methods: {
            showPhoto() {
                this.isShow = !this.isShow
            }
        }
 
    }
</script>

<style>
    .show {
        z-index:98; 
        position: fixed;
        top:5vh;
        left:20%;
    }
    .showPhoto {
        height: 90vh;
        width: auto;
        cursor:default;        
    }
    .showPhoto:hover {
        filter: none;
    }
    .closeBtn {
        z-index:99;
        width:50px;
        height: 50px;
        background-color: black;
        color:white;
        font-size:30px;
        font-weight: bold;
        opacity:.7;
        position:absolute;
        border:none;
        border-radius:0 8px 0 8px;
        top:0;
        right:0;
        cursor:pointer;
    }
    .closeBtn:hover {
        opacity:.9;
    }
    
</style>