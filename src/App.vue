<script>
import NavbarComponent from './components/NavbarComponent.vue'
import MainComponent from './components/MainComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
export default {
  components: {
    NavbarComponent,
    MainComponent,
    FooterComponent,
    HeaderComponent
  }


}
</script>

<template>
  <div>
    <nav id="csss">
      <navbar-component></navbar-component>
    </nav>
    <header>
      <header-component></header-component>
    </header>
    <main>
      <main-component></main-component>
    </main>
    <footer>
      <footer-component></footer-component>
    </footer>


  </div>
</template>

<style scoped></style>
