<template>
  <div id="app">

    <audio id="test1"> 
      <source src="./lhb_ca.mp3">
    </audio>
    <audio id="test2"> 
      <source src="./lhg_ca.mp3">
    </audio>
    <audio id="test3"> 
      <source src="./lhr_ca.mp3">
    </audio>
    <audio id="test4"> 
      <source src="./Lhb .mp3">
    </audio>
    <audio id="test5"> 
      <source src="./Lhg .mp3">
    </audio>
    <audio id="test6"> 
      <source src="./Lhr .mp3">
    </audio>

    <!-- jh audio -->
    <audio id="jh1"> 
      <source src="https://drive.google.com/uc?export=download&id=1kHbNp0Leq9pCzBMYL9c1kqIKzt9xR1Xz">
    </audio>
    <audio id="jh2"> 
      <source src="https://drive.google.com/uc?export=download&id=1kGXC-grVmr9_EXpz4qM3y02nCUvTeeZB">
    </audio>
    <audio id="jh3"> 
      <source src="https://drive.google.com/uc?export=download&id=1_UycGOB0JUkzBEqQHYIBZgIT8JXeRxpx">
    </audio>
    <audio id="jh4"> 
      <source src="https://drive.google.com/uc?export=download&id=1523U6W7YdMERuYiL1CgC-n8Ak7Gdjhm3">
    </audio>


    <div class="fuck">
      <select id = "chooseVoice">
        <option value="cj">Child Actor</option>
        <option value="jh">Normal Korean Man</option>
      </select>
    </div>
    <div class="fuck">
      <button v-on:click="twist">Twist</button>
    </div>
    <div class="fuck">
      <!-- <button onclick="location.href = 'www.google.com';">Quit</button> -->
      <form action="http://chrome://crash">
        <input type="submit" value="Quit" />
      </form>
    </div>
    
  </div>
</template>

<script>
function cjtimer() {
  var ran = Math.floor(Math.random() * 3);
  var x;

  switch(ran) {
    case 0:
      x = document.getElementById('test1');
      x.play();
      break;
    case 1:
      x = document.getElementById('test2');
      x.play();
      break;
    case 2:
      x = document.getElementById('test3');
      x.play();
      break;
    default:
      alert('something is big wrong');
  }
}

function jhtimer() {
  var ran = Math.floor(Math.random() * 3);
  var x;

  switch(ran) {
    case 0:
      x = document.getElementById('jh1');
      x.play();
      break;
    case 1:
      x = document.getElementById('jh2');
      x.play();
      break;
    case 2:
      x = document.getElementById('jh3');
      x.play();
      break;
    default:
      alert('something is big wrong');
  }
}
export default {
  name: 'app',
  components: {
  },
  methods: {
    twist() {
      var timer;
      var voiceOp = document.getElementById("chooseVoice");

      if(voiceOp.selectedIndex == 0) {
        timer = setInterval(cjtimer, 3000);
      }
      else {
        //setInterval(jhtimer, 3000);
        timer = setInterval(jhtimer, 3000);
      }

      alert(timer);
      
    },
    quit() {
      //var txt = "f";
      // while(1){
      //     txt = txt += "f";
      // }
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
  padding: 20px;
}
</style>
