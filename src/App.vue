<template>
  <header>
    <NavBarComponent />
  </header>
  
  <div id="content">
    <section id="head-section">
      <HeadComponent />
    </section>

    <section id="about-section">
      <AboutComponent />
    </section>

    <section id="works-section">
      <div>
        <ExpComponent />
      </div>
      <div>
        <ProjectComponent />
      </div>
    </section>

    <section id="contact-section">
      <ContactComponent />
    </section>
  </div>

  <footer>
    <div>
      <h4>
          <a id="site-repo" href="https://github.com/devbcdestiller/devbcdestiller.github.io" target="_blank">Built by Brian Estiller</a>
      </h4>
    </div>
  </footer>

</template>

<script setup>
import NavBarComponent from './components/NavBarComponent.vue'
import HeadComponent from './components/HeadComponent.vue'
import AboutComponent from './components/AboutComponent.vue'
import ExpComponent from './components/ExpComponent.vue'
import ProjectComponent from './components/ProjectComponent.vue'
import ContactComponent from './components/ContactComponent.vue'
</script>

<style>
@keyframes fadeIn{
  from {opacity: 0;}
  to {opacity: 1;}
}

#content {
  margin: 8vw auto;
  width: clamp(480px, 70%, 1600px);
  line-height: 1.5;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  row-gap: max(375px, 40vh);
  animation: fadeIn 1.5s 1;
}

html {
  scroll-behavior: smooth;
} 

section {
  scroll-margin-top: max(100px, 6vw);
  scroll-margin-bottom: 6vw;
}

header {
  top: 0;
  position: sticky;
  position: -webkit-sticky;
  background-color: #353535;
  z-index: 2;

}

body {
  font-family: Arial, Helvetica, sans-serif;
  padding: 0;
  margin: 0;
  background-color: #353535;
}

h1 {
  color: white;
}

p, h2 {
  color: #b4b4b4;
}

a {
  text-decoration: none;
  color: white;
}

footer {
  text-align: center;

  font-family: 'Courier New', Courier, monospace;
}

#site-repo {
  color: white;
  transition: color 0.2s;
}

#site-repo:hover {
  color: #202020;
}


</style>
