# Ball-rolling-welcome
Animated welcome page

<style>
/*need to sort out responsiveness*/

#main-container { /*none of this makes a difference to centering all but flex and flex-direction is now working*/
  display: flex;
  flex-direction: column;
  width: 100%;
  justify-content: center;
  margin: auto auto; 
  
  /*BELOW CSS IS JUST TO SHOW THE #MAIN-CONTAINER*/
  
  border: 4px solid blue;
  width: 100vw;
  min-width: 470px;
  height: 100%;
  border-radius: 30px;
}

#welcome-div { 
  width: 30vw;
  background-color: red;
  transform: skewX(-20deg) translateX(20px);
  animation: slide-in 1s;
  animation-direction: right;
  margin: auto auto;
}

@keyframes slide-in {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(1);
  }
}

#welcome {
  font-family: Rubik;
  margin: auto auto;
  font-size: 6vw;
}

#gettheballrollingtext {
  font-family: Rubik;
  margin: auto auto;
  font-size: 4vw;
}

#ballrollingtext-div {
  width: 51%;
  background-color: yellow;
  transform: skewX(-20deg) translateX(20px);
  animation: slide-in 4s;
  animation-direction: right;
  margin: auto auto;
}

#ballpath-div {
  min-height: 40px;
  width: 250px; 
  transform: translateX(20px);
  animation: slide-in 7s;
  animation-direction: right;
  margin: auto auto;
}

#ball-outer {
  position: relative;
  background-color: black;
  border: 2px solid black;
  border-radius: 50%;
  width: 30px;
  height: 30px;
  float: left; 
	transition: 2.5s linear;
}

#ball-inner {
  position: relative;
  background-color: white;
  border: 1px solid white;
  border-radius: 50%;
  width: 7px;
  height: 7px;
  margin: 3px;
}

#ball-line {
  background-color: black;
  height: 4px;
  width: 250px;
  transform: translate(20px);
  animation: slide-in 7s;
  animation-direction: right; 
  margin: auto auto;
}

#ball-line-dot {
  width: 4px;
  height: 4px;
  background-color: white;
  transform: translate(250px);
  animation: ballLineSlider 10s; 
  animation-direction: right;
}

@keyframes ballLineSlider {
  0% {
    transform: translateX(0);
  }
  25% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(1);
  }
}

#ball-button {
  border: 2px solid black;
  border-radius: 8px;
  font-family: verdana;
  height: 65px;
  width: 65px; 
}

#ball-button:hover {
  cursor: pointer;
  background-color: purple; 
}

#button-glow {
  padding: 10px 0 10px 0;
  text-align: center;
  background-color: blue;
  width: 75px;
  height: 65px;
  border: 2px solid black;
  border-radius: 8px;
}

.center {
  display: flex;
  justify-content: center;
}

#div-to-center-button {
  animation: fadein 14s;
}

@keyframes fadein{
  0% { opacity:0; }
  25% { opacity:0; }
  50% { opacity:0; }
  65% {opacity:0;}
  100% { opacity:1; }
}

#i-design { 
  background-color: black;
  color: white;
  width: 20%;
  font-family: verdana;
  font-size: 2em;
  min-width: 180px;
  margin: auto auto;
}

#i-container {
  width: 100%;
  min-height: 200px;
  justify-content: center;
  margin: auto auto;
}

#i-program { 
  background-color: black;
  color: white;
  width: 20%;
  font-family: verdana;
  font-size: 2em;
  min-width: 180px;
  margin: auto auto;
}

#i-create {
  background-color: black;
  color: white;
  width: 20%;
  font-family: verdana;
  font-size: 2em;
  min-width: 180px;
  margin: auto auto;
}

#i-inspire {
  background-color: black;
  color: white;
  width: 20%;
  font-family: verdana;
  font-size: 2em;
  min-width: 180px;
  margin: auto auto;
}

</style>

<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />  
  <title>Ball rolling</title>
  <link rel="stylesheet" type="text/css" href="styles.css" />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Rubik:wght@800&display=swap" rel="stylesheet" />
  <link href="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js" />
  <link href="https://cdn.skypack.dev/bootstrap@5.1.3"/>
</head>

<!DOCTYPE html>
  
<html>
  <body id="body">
    <div id="main-container" >
      <div id="welcome-div">
        <header id="welcome">WELCOME</header> 
      </div>
  
      <div id="ballrollingtext-div">
        <header id="gettheballrollingtext">Let's get the ball rolling!</header>    
      </div>
      <br></br>
      <div id="ballpath-div">    
        <div id="ball-outer">
          <div id="ball-inner"></div>
        </div>
      </div>
      <div id="ball-line">
        <div id="ball-line-dot"></div>
      </div>
      <br></br>
      <div id="div-to-center-button" class="center">
        <div id="button-glow">    
          <button id="ball-button">PRESS</button>
        </div>
      </div>
      <br></br>
      <div id="i-container">
        <div id="i-design">Design</div>
        <br></br>
        <div id="i-program">Program</div>
        <br></br>
        <div id="i-create">Create</div>
        <br></br>
        <div id="i-inspire">Inspire</div>
      </div>
    </div>
  </div>
<body>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<script>
import * as bootstrap from "https://cdn.skypack.dev/bootstrap@5.1.3";

//* ROTATES AND SLIDES BALL/ also produces animations for button onclick

let startingAngle = 0;

$("#ball-button").on('click', function() {
	startingAngle += 720;

	$("#ball-outer").css({transform: "rotate(" + startingAngle + "deg"});
	$("#ball-inner").css({transform: "rotate(-" + startingAngle + "deg"});
  $('#ball-outer').animate({"marginLeft": "+=210px"});
  $('#div-to-center-button').delay(2000).fadeOut(3000);
  $('#ball-outer, ball-inner, ballpath-div').delay(1000).fadeOut(3000);
  $('#ball-line, ball-line-dot').delay(3000).fadeOut(3000);    
  $('#gettheballrollingtext').delay(3000).fadeOut(3000);  
  $('#welcome').delay(3000).fadeOut(3000);
  $('#i-container').delay(7000).animate({"marginTop": "-=110px" });
  $('#i-program').delay(8000).animate({"marginTop": "-=10px"});
  $('#i-create').delay(9000).animate({"marginTop": "-=10px"});
  $('#i-inspire').delay(10000).animate({"marginTop": "-=10px"});
});
</script>
</html>
  
