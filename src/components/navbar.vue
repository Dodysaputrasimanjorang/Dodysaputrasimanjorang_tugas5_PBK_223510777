<template>

  <div class="q-pa-none" id="navbar">
   <q-toolbar class="bg-black text-white ">
     <h3>Simanjorang Diamond</h3>
   </q-toolbar>
   
 
 </div>
</template>

<script>
import { ref } from 'vue'

export default {
 setup () {
   return {
     model: ref('one'),
   }
 }
}
</script>

<style>

.gambar {
 width: 50%;
 height: 50%;
}

.input-container {
 width: 460px;
 position:relative;

}

.icon {
 position: absolute;
 right: 10px;
 top: calc(50% + 5px);
 transform: translateY(calc(-50% - 5px));
}

.input {
 width: 100%;
 height: 40px;
 padding: 10px;
 transition: .2s linear;
 border: 2.5px solid black;
 font-size: 14px;
 text-transform: uppercase;
 letter-spacing: 2px;
}

.input:focus {
 outline: none;
 border: 0.5px solid black;
 box-shadow: -5px -5px 0px black;
}

.input-container:hover > .icon {
 animation: anim 1s linear infinite;
}

@keyframes anim {
 0%,
 100% {
   transform: translateY(calc(-50% - 5px)) scale(1);
 }

 50% {
   transform: translateY(calc(-50% - 5px)) scale(1.1);
 }
}

</style>
