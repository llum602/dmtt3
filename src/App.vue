<template>
  <div id="app">

    <!-- <audio id="test">
      <source src="src\assets\music\test.mp3">
    </audio>
    <audio ref="audioRef" src="test.mp3"></audio> -->

    <audio ref="aRef" id="aRef" src="/public/test1.ogg"></audio>

    <div class="fuck">
      <button v-on:click="twist">Twist</button>
    </div>

    <div class="fuck">
      <button type="button">Quit</button>
    </div>

  </div>
</template>

<script>
//import {Howl} from 'howler';
//require('howler');

// function dipshit() {
//   //alert('ass');
//   var ran = Math.floor(Math.random() * 1);
//   //var x;

//   switch(ran) {
//     case 0:
//       //alert('0');
//       var sound = new Howl({
//         src: ['Recording-3.mp3']
//       });

//       sound.play();
//       break;
//     case 1:
//       // x = document.getElementById('test');
//       // x.play();
//       break;
//     case 2:
//       alert('2');
//       break;
//     case 3:
//       alert('3');
//       break;
//     case 4:
//       alert('4');
//       break;
//     case 5:
//       alert('5');
//       break;
//     case 6:
//       alert('6');
//       break;
//     case 7:
//       alert('7');
//       break;
//     case 8:
//       alert('8');
//       break;
//     case 9:
//       alert('9');
//       break;
//     case 10:
//       alert('10');
//       break;
//     case 11:
//       alert('11');
//       break;
//     case 12:
//       alert('12');
//       break;
//     case 13:
//       alert('13');
//       break;
//     case 14:
//       alert('14');
//       break;
//     case 15:
//       alert('15');
//       break;
//     case 16:
//       alert('16');
//       break;
//     case 17:
//       alert('17');
//       break;
//     default:
//       alert('something is big wrong');
//   }

//   //x.pause();
// }

export default {
  name: 'app',
  components: {
  },
  methods: {
    twist: function () {
      //setInterval(dipshit, 3000);
      alert('hi');
      // var sound = new Howl({
      //   src: ['../public/test.mp3'],
      //   html15: true,
      //   autoplay: true,
      //   volume: 1.0
      // });

      // sound.play();

      this.$refs.aRef.play();


    }
    
  }
}


</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.fuck {
  text-align: center;
  background-color: red;
}
</style>
