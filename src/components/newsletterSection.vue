<script>

import store from '../dataset/store.json'

export default {
  name: 'newsletterSection',
  data() {
    return {
      store
    }
  },
  methods: {
    // Aggiunge indirizzo email e nome dell'utente all'elenco di iscritti alla newsletter

    subscribe(e) {

      e.preventDefault();
      store.subscribers.push({
        name: store.userName,
        email: store.userEmail
      });

      store.userName = '';
      store.userEmail = '';

      console.log(store.subscribers);
    },


  }
}


</script>

<template>
  <section id="newsletter">

    <!-- Descrizione newsletter -->

    <div id="newsletter-description">
      <h5>NEWSLETTER</h5>
      <div id="name">
        <div id="background">
          <h2>Know</h2>
        </div>
        <H2>First</H2>
      </div>
      <p>Follow closely and receive content about our company and the news of the current market.</p>
    </div>

    <!-- Form iscrizione newsletter -->

    <div id="newsletter-form">
      <form id="subscription" v-on:submit="subscribe">
        <input type="text" id="name" placeholder="Name" v-model="store.userName" required>
        <input type="email" id="email" placeholder="Email" v-model="store.userEmail" required>
        <button type="submit">SUBSCRIBE</button>
      </form>
    </div>

  </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

#newsletter {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  padding: 50px 0;
  background-image: url(../assets/img/bg-1.jpg);
  background-position: center;
  background-size: cover;
  color: white;

  // Regole comuni dei componenti della sezione

  #newsletter-description,
  #newsletter-form {
    width: calc(100% / 4 - 100px);
    margin-left: 100px;
  }

  // Regole descrizione newsletter

  #newsletter-description {
    text-align: justify;

    h5,
    #name,
    p {
      margin-bottom: 30px;
    }

    #name {
      h2 {
        margin-left: 10px;
        font-size: 30px;
      }
    }
  }

}
</style>