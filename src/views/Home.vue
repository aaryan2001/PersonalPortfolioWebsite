<template>
	<div>
    <div class="parallax">
      <div class="paratext">
      <br><br><br><br>
      <p class="line-1 anim-typewriter">Hello, Welcome to my portfolio website.</p>
      </div>
    </div>
    <br><br>
    <div class="container">
      <div class="col-sm">
      
        <img src="../assets/me.png" alt="Aaryan Pujara" style="float:left;width:300px;height:300px;margin:50px 50px;">
        <br>
        <br>
        <h1 class="intro">My name is Aaryan Pujara.</h1>
        <h2 class="a">About me</h2>
        <p class="a">I am a Bachelor of Computer Science student who loves to learn and work on new things. I am always looking for opportunities where I can enhance my skills and get exposure. I love taking up challenges and meet new people.I am a very socially outgoing person and love to have a chat over a beer any day.I am a fun guy who likes to grab a beer after finishing work and love to rewatch The Office every now and then. I love to go out and explore and go on adventures.</p>
        <br><br><br>
      </div>
    </div>
    <div class ="col-sm">
      <h2 class="h"> My interests and hobbies. </h2>
      <p class="h">I love to learn new things and skills in my free time but my top hobbies are:</p>
      <ul class="hl">
        <li>Making Coffee art</li>
        <li>Web development free lancing</li>
        <li>Listening to music</li>
        <li>Producing music</li>
        <li>Skateboarding</li>
      </ul>
      <div>
	</div>
    </div>
  </div>
</template>

<style>


/* Global */

.line-1{
    position: relative;
    top: 50%;  
    width: 24em;
    margin: 400px 50px;
    border-right: 2px solid rgba(255,255,255,.75);
    font-size: 350%;
    font-family: "Andale Mono", monospace;
    text-align: left;
    white-space: nowrap;
    overflow: hidden;
    transform: translateY(-50%);    
}

/* Animation */
.anim-typewriter{
  animation: typewriter 4s steps(44) 1s 1 normal both,
             blinkTextCursor 500ms steps(44) infinite normal;
}
@keyframes typewriter{
  from{width: 0;}
  to{width: 24em;}
}
@keyframes blinkTextCursor{
  from{border-right-color: black;}
  to{border-right-color: transparent;}
}

.parallax {
  /* The image used */
  background-image: url('../assets/paraimage.gif');

  /* Full height */
  min-height: 950px;
  min-width: 120%; 
  margin: -200px 0px 0px -20px;

  /* Create the parallax scrolling effect */
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

@media screen and (max-width: 1090px) {
.parallax {display: none;}
}
</style>

<script>

</script>
