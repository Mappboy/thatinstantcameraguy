<script>
const PRINT_AUDIO = new Audio(
  'https://www.soundjay.com/mechanical/sounds/polaroid-camera-take-picture-02.mp3'
)

export default {
  methods: {
    clickShutter() {
      document.getElementById('s1').style.animation = 'print 4.5s'
      document.getElementById('b').style.animation = ' show 7s 4.5s'
      document.getElementById('b').style.opacity = '0'
      document.getElementById('s1').style.top = '60px'
      PRINT_AUDIO.play()
    }
  }
}
</script>

<template>
  <v-container>
    <div>
      <div class="cont1">
        <div class="top"></div>
        <div class="printerin">
          <div id="s1">
            <div id="b">
              <p>Coming Soon</p>
            </div>
          </div>
        </div>
        <div class="printer"></div>

        <div class="upper">
          <div class="rainbow1"></div>
        </div>
        <div class="downer">
          <div class="rainbow"></div>
        </div>
        <div class="lense"></div>
        <button class="button" @click="clickShutter" />
        <div class="flash"></div>
        <div class="nod"></div>
        <div class="label">
          <h3>Fixed</h3>
        </div>
      </div>
    </div>
  </v-container>
</template>

<style scoped>
body {
  text-align: center;
}
h3 {
  font-family: 'Bungee Shade', cursive;
  font-size: 28px;
}
.cont1 {
  position: absolute;
  top: 100px;
  width: 100%;
  text-align: center;
  perspective: 100px;
  margin-bottom: 600px;
}
.upper {
  position: absolute;
  left: 50px;
  width: 350px;
  height: 150px;
  border-radius: 20px 20px 0px 0px;
  background: white;
}
.downer {
  position: absolute;
  top: 150px;
  left: 47.5px;
  width: 355px;
  height: 60px;
  border-radius: 0px 0px 0px 0px;
  background: linear-gradient(rgb(240, 240, 240), white);
  tarnsform-style: preserve-3d;
  transform: rotatex(3deg);
  perspective: 100px;
}
.printer {
  position: absolute;
  top: 213px;
  left: 45px;
  width: 362px;
  height: 35px;
  background: rgb(30, 30, 30);
}
.printer::after {
  content: '';
  position: absolute;
  top: 20px;
  left: 40px;
  width: 280px;
  height: 15px;
  border-radius: 10px 10px 0px 0px;
  background: rgb(50, 50, 50);
}
.printerin {
  position: absolute;
  top: 248px;
  left: 45px;
  width: 362px;
  height: 35px;
  border-radius: 0px 0px 20px 20px;
  background: rgb(30, 30, 30);
}
.printerin::before {
  content: '';
  position: absolute;
  top: 0px;
  left: 40px;
  width: 280px;
  height: 15px;
  border-radius: 0px 0px 10px 10px;
  background: rgb(50, 50, 50);
}
.rainbow2 {
  position: absolute;
  top: -20px;
  left: 157px;
  height: 20px;
  width: 50px;
  background-image: repeating-linear-gradient(
    to right,
    #ef0079 0px,
    #ef0079 10px,
    #d70006 10px,
    #d70006 18px,
    #ff9c00 18px,
    #ff9c00 26px,
    #feeb00 26px,
    #feeb00 34px,
    #5db333 34px,
    #5db333 42px,
    #00b2ff 42px,
    #00b2ff 50px
  );
  opacity: 0.7;
}
.lense {
  position: absolute;
  top: 31px;
  left: 171px;
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background: black;
  border: 4px solid rgb(50, 50, 50);
  box-shadow: -10px 10px 30px rgb(50, 50, 50);
}
.lense::after {
  content: '';
  position: absolute;
  left: 10px;
  top: 25px;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background: white;
}
.lense::before {
  content: '';
  position: absolute;
  left: 20px;
  top: 20px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: white;
  opacity: 0.5;
}
.button {
  position: absolute;
  left: 100px;
  top: 90px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: #ff0200;
  border: 3px solid rgb(230, 230, 230);
  cursor: pointer;
  box-shadow: 0px 0px 5px black;
  outline: none;
}
.button:focus {
  position: absolute;
  left: 100px;
  top: 90px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: #c62828;
  border: 3px solid rgb(230, 230, 230);
  cursor: pointer;
  box-shadow: 0px 0px 5px black;
  outline: none;
}
.flash {
  position: absolute;
  left: 300px;
  top: 30px;
  width: 70px;
  height: 50px;
  background: repeating-linear-gradient(
    to right,
    grey,
    grey 10px,
    rgb(50, 50, 50) 10px,
    rgb(50, 50, 50) 20px
  );
  border: solid;
}
.nod {
  position: absolute;
  left: 315px;
  top: 96px;
  width: 25px;
  height: 25px;
  border-radius: 50%;
  background: rgb(20, 20, 20);
  border: 5px solid rgb(50, 50, 50);
}
.label {
  position: absolute;
  left: 70px;
  top: 30px;
  width: 90px;
  height: 40px;
  background: rgb(30, 30, 30);
  border-radius: 10px 10px 10px 10px;
  text-align: center;
}
.label h3 {
  position: absolute;
  top: -10px;
  left: 10px;
  color: white;
  font-family: 'Roboto', sans-serif;
}
.rainbow1 {
  opacity: 0.8;
  position: absolute;
  top: 50px;
  left: 153px;
  height: 130px;
  width: 48px;
  background-image: repeating-linear-gradient(
    to right,
    #ef0079 0px,
    #ef0079 8px,
    #d70006 8px,
    #d70006 16px,
    #ff9c00 16px,
    #ff9c00 24px,
    #feeb00 24px,
    #feeb00 32px,
    #5db333 32px,
    #5db333 40px,
    #00b2ff 40px,
    #00b2ff 48px
  );
}
.rainbow {
  position: absolute;
  top: -2px;
  left: 155px;
  height: 61px;
  width: 48px;
  background-image: repeating-linear-gradient(
    to right,
    #ef0079 0px,
    #ef0079 8px,
    #d70006 8px,
    #d70006 16px,
    #ff9c00 16px,
    #ff9c00 24px,
    #feeb00 24px,
    #feeb00 32px,
    #5db333 32px,
    #5db333 40px,
    #00b2ff 40px,
    #00b2ff 48px
  );
  tarnsform-style: preserve-3d;
  transform: rotatex(10deg);
}
#s1 {
  position: absolute;
  top: -240px;
  left: 60px;
  width: 230px;
  height: 180px;
  border: 5px solid white;
  border-bottom: 30px solid white;
  box-shadow: 0px 0px 40px black;
  background: url('https://cdni.rbth.com/rbthmedia/images/all/2017/05/28/russia_selfie.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  transition: 0.5s;
  transfrom-origin: top;
}
#b {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 230px;
  height: 180px;
  background: black;
  transition: 0.5s;
  transfrom-origin: top;
}
.top {
  position: absolute;
  top: -10px;
  left: 100px;
  background: rgb(40, 40, 40);
  width: 250px;
  height: 20px;
  border-radius: 10px 10px 0px 0px;
}

@keyframes print {
  0% {
    top: -240px;
    background: rgb(0, 0, 0);
  }
  10% {
    top: -200px;
    background: rgb(0, 0, 0);
  }
  20% {
    top: -150px;
    background: rgb(0, 0, 0);
  }
  30% {
    top: -100px;
    background: rgb(0, 0, 0);
  }
  40% {
    top: -50px;
    background: rgb(0, 0, 0);
  }
  50% {
    top: -10px;
    background: rgb(0, 0, 0);
  }
  60% {
    top: 0px;
    background: rgb(0, 0, 0);
  }
  100% {
    top: 60px;
    background: rgb(0, 0, 0);
  }
}
@keyframes show {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
</style>
