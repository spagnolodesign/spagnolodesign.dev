<template>
  <div class="container">
    <div>
      <h2 class="title bring-up">Buonasera</h2>
      <h2 class="title title-black">Simplicity</h2>
    </div>
    <div class="description">
      <p>I’m Luca Spagnolo, a software engineer that loves to create and build extraordinary ideas.</p>
      <br><br><br>
      <p class="underline">Services</p>
      <ul class="list">
        <li>App Development</li>
        <li>Web Development</li>
      </ul>
      <br>
      <a  target="_blank" href="mailto:luca.spagnolo91@gmail.com" class="link">Get in touch</a>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  head: {
    title: 'Luca Spagnolo - Software engineer',
    meta: [
      { hid: 'description', name: 'description', content: 'I’m Luca Spagnolo, a software engineer that loves to create and build extraordinary ideas. Services: App Development, Web Development' }
    ]
  },
  components: {
    Logo
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Playfair+Display&display=swap');

body{
  background: #1C1C1C;
  font-family: 'Courier', Courier, monospace;
  font-size: 100%;
  -webkit-touch-callout: none;
  min-height: 100vh;
  -webkit-text-size-adjust: 100%;
  -webkit-font-smoothing: antialiased;
   color: #FFF;
   font-weight: 100;
}

h1, 
h2, 
h3, 
h4, 
h5, 
h6 {
  font-family: 'Playfair Display', serif;
  font-weight: 100;
}

p, a, ul{
  font-size: 1.3em;
}

.container {
  display: flex;
  min-height: 100vh;
  align-items: center;
}

.underline{
  text-decoration: underline;
}

.list {
  margin: 0.2em 0 1em 0; 
}

.link{
  text-decoration: none;
  color:#FFF;
  z-index: 1;
}

a{
  position: relative; 
}

a:after{
  content: " ";
  width: 105%;
  height: 10px;
  background: rgb(41, 41, 41);;
  display: block;
  position: absolute;
  bottom: 2px;
  z-index: -1;
  transition: .4s;
  left: -5px;
}


a:hover:after{
  width: 0;
  height: 8px;
  right: 0;
}

@media (min-width: 600px) {
  .container > div {
    width: 50%;
    margin-top: -6em;
  }
  .title {
    font-size: 6.5em;
    color: #FFF;
    line-height: 1em;
    margin-left: 1.3em;
  }
  .bring-up{
    margin-top: -1.2em; 
  }
  .title-black {
    color: black;
  }
  .description {
    padding: 0em 7em 0 4em;
  }
  .description .link{
    margin-top: 1em;
  }
}
</style>
