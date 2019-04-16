<script>
  const PRINT_AUDIO = new Audio("https://www.soundjay.com/mechanical/sounds/polaroid-camera-take-picture-02.mp3");

  export default {
    methods: {
      clickShutter() {
        document.getElementById("s1").style.animation = "print 4.5s";
        document.getElementById("b").style.animation = " show 7s 4.5s";
        document.getElementById("b").style.opacity = "0";
        document.getElementById("s1").style.top = "60px";
        PRINT_AUDIO.play();
      }

    },
  }
</script>

<template>
  <div>
    <div class="cont1">
      <div class="top"></div>
      <div class="printerin">
        <div id="s1">
          <div id="b"></div>
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
      <button class="button" v-on:click="clickShutter"/>
      <div class="flash"></div>
      <div class="nod"></div>
      <div class="lable">
        <h3>OneStep</h3>
      </div>
    </div>
  </div>
</template>

<style scoped>
  h2 {
    margin-top: 0px;
    margin-left: 30px;
    font-family: 'Bungee Shade', cursive;
    font-size: 45px;
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
    left: 550px;
    width: 350px;
    height: 150px;
    border-radius: 20px 20px 0px 0px;
    background: white;
  }

  .downer {
    position: absolute;
    top: 150px;
    left: 547.5px;
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
    left: 545px;
    width: 362px;
    height: 35px;
    background: rgb(30, 30, 30);
  }

  .printer::after {
    content: "";
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
    left: 545px;
    width: 362px;
    height: 35px;
    border-radius: 0px 0px 20px 20px;
    background: rgb(30, 30, 30);

  }

  .printerin::before {
    content: "";
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
    background-image: repeating-linear-gradient(to right,
    #EF0079 0px, #EF0079 10px,
    #D70006 10px, #D70006 18px,
    #FF9C00 18px, #FF9C00 26px,
    #FEEB00 26px, #FEEB00 34px,
    #5DB333 34px, #5DB333 42px,
    #00B2FF 42px, #00B2FF 50px);
    opacity: .7;
  }

  .lense {
    position: absolute;
    top: 31px;
    left: 671px;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    background: black;
    border: 4px solid rgb(50, 50, 50);
    box-shadow: -10px 10px 30px rgb(50, 50, 50);
  }

  .lense::after {
    content: "";
    position: absolute;
    left: 10px;
    top: 25px;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background: white;

  }

  .lense::before {
    content: "";
    position: absolute;
    left: 20px;
    top: 20px;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: white;
    opacity: .5;
  }

  .button {
    position: absolute;
    left: 600px;
    top: 90px;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: #FF0200;
    border: 3px solid rgb(230, 230, 230);
    cursor: pointer;
    box-shadow: 0px 0px 5px black;
    outline: none;
  }

  .button:focus {
    position: absolute;
    left: 600px;
    top: 90px;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: #C62828;
    border: 3px solid rgb(230, 230, 230);
    cursor: pointer;
    box-shadow: 0px 0px 5px black;
    outline: none;
  }

  .flash {
    position: absolute;
    left: 800px;
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
    left: 815px;
    top: 96px;
    width: 25px;
    height: 25px;
    border-radius: 50%;
    background: rgb(20, 20, 20);
    border: 5px solid rgb(50, 50, 50);
  }

  .lable {
    position: absolute;
    left: 570px;
    top: 30px;
    width: 90px;
    height: 40px;
    background: rgb(30, 30, 30);
    border-radius: 10px 10px 10px 10px;
    text-align: center;
  }

  .lable h3 {
    position: absolute;
    top: -10px;
    left: 10px;
    color: white;
    font-family: 'Roboto', sans-serif;
  }

  .rainbow1 {
    opacity: .8;
    position: absolute;
    top: 50px;
    left: 153px;
    height: 130px;
    width: 48px;
    background-image: repeating-linear-gradient(to right,
    #EF0079 0px, #EF0079 8px,
    #D70006 8px, #D70006 16px,
    #FF9C00 16px, #FF9C00 24px,
    #FEEB00 24px, #FEEB00 32px,
    #5DB333 32px, #5DB333 40px,
    #00B2FF 40px, #00B2FF 48px);
  }

  .rainbow {
    position: absolute;
    top: -2px;
    left: 155px;
    height: 61px;
    width: 48px;
    background-image: repeating-linear-gradient(to right,
    #EF0079 0px, #EF0079 8px,
    #D70006 8px, #D70006 16px,
    #FF9C00 16px, #FF9C00 24px,
    #FEEB00 24px, #FEEB00 32px,
    #5DB333 32px, #5DB333 40px,
    #00B2FF 40px, #00B2FF 48px);
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
    background: url('https://www.facebook.com/photo.php?fbid=10212570648681351&set=a.3265034424883&type=3&eid=ARAC_qlrghWCE-eDxLA2H2FXcl-CeN-akhKKSnzT9AP3bZtYwg0N7ng03qG-NPNyuBgG69WM0_QmOnP2');
    background-repeat: no-repeat;
    background-size: cover;
    transition: .5s;
    transfrom-origin: top;

  }

  #b {
    position: absolute;
    top: 0px;
    left: 0px;
    width: 230px;
    height: 180px;
    background: black;
    transition: .5s;
    transfrom-origin: top;
  }

  .top {
    position: absolute;
    top: -10px;
    left: 600px;
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
