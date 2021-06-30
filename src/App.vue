<template>
  <div id="app">
  <a href="/" class="logo">Aaryan Pujara / Resume</a>

    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/experience">Experience</router-link> |
      <router-link to="/education">Education</router-link> |
      <router-link to="/skills">Skills</router-link> |
      <router-link to="/contact">Contact</router-link>
    </div>
    <router-view/>
      <!-- bootstrap -->
  <link href="../assets/css/bootstrap.min.css" rel = "stylesheet" />

    <footer>
      <div>
        <p>Author: Aaryan Pujara (102599490)</p>
        <p><a href="mailto:102599490@student.swin.edu.au">102599490@student.swin.edu.au</a></p>
      </div>
    </footer>
  </div>
</template>

<style>

.container {
  transition: transform .2s; /* Animation */
}

.container:hover {
  transform: scale(1.05); /* (150% zoom - Note: if the zoom is too large, it will go outside of the viewport) */
  background-color: rgb(255, 197, 145);
}

h1{
  text-align: centre;
  margin: 30px 140px;
}

body {
  background-color: white;
}

div.container{
  background-color: rgb(255,218,185);
}

.h{
  text-align:left;
  margin: 15px 50px;
}

h2.h{
  margin: 20px 45px;
}

.a{
  margin: 15px 100px;
}
h2.a{
  margin: 20px 100px;
}
ul {
  text-align: left;
  display: block;
  list-style-type: disc;
}
.hl {
  margin: 0px 35px;
}

footer{
  padding: 30px 80px;
  color: black;
}

.logo{
  font-size: 25px;
  font-weight: bold;
  color: black;
  text-decoration: none;
  font-family: "Andale Mono", monospace;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  overflow: hidden;
  background-color: #f1f1f1;
  padding: 20px 10px;
}

#nav {
  padding: 30px 80px;
}

#nav a {
  font-weight: bold;
  color: rgb(79, 78, 78);
}

#nav a:hover {
  background-color: rgb(163, 158, 158, 0.3);
}

#nav a.router-link-exact-active {
  color: #fa7c73;
}
</style>
