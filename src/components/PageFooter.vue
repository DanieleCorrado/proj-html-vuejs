<script>
import contacts from '../dataset/contacts.json';
import about from '../dataset/about.json';
import transport from '../dataset/transport.json';
import support from '../dataset/support.json';

export default {
  name: "PageFooter",
  data() {
    return {
      contact: contacts,
      about: about,
      transport: transport,
      support: support
    }
  }
}
</script>

<template>
  <footer>


    <section id="information">

      <!-- Sezione contatti azienda -->

      <div id="contact">

        <div id="background">
          <h2>NEX</h2>
        </div>

        <H2>GEN</H2>

        <p>
          A funcional HTML template for corporate and business.
        </p>

        <ul>

          <li>
            <font-awesome-icon icon="fa-solid fa-phone" />
            <span id="phone">
              +{{ contact[0].stateCode }}
              <span v-if="contact[0].areaCode">({{ contact[0].areaCode }})</span>
              {{ contact[0].phoneNumber }}
            </span>
          </li>

          <li>
            <font-awesome-icon icon="fa-solid fa-envelope" />
            <span id="mail"> {{ contact[1].mail }} </span>
          </li>

          <li>
            <font-awesome-icon icon="fa-solid fa-location-dot" />
            <span>{{ contact[2].streetName }}, {{ contact[2].houseNumber }}</span>
          </li>

        </ul>

        <button type="button"> GET IN TOUCH</button>

      </div>

      <!-- Sezione informazioni azienda -->

      <div id="about">

        <h2>About</h2>

        <ul>
          <li v-for="option in about">
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
            <a :href="option.linkSection">{{ option.nameSection }}</a>
          </li>
        </ul>

      </div>

      <!-- Sezione trasporti -->

      <div id="transport">
        <h2>Transport</h2>

        <ul>
          <li v-for="option in transport">
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
            <a :href="option.linkSection"> {{ option.nameSection }}</a>
          </li>
        </ul>
      </div>

      <!-- Sezione supporto -->

      <div id="support">
        <h2>Support</h2>

        <ul>
          <li v-for="option in support">
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
            <a :href="option.linkSection">{{ option.nameSection }}</a>
          </li>
        </ul>
      </div>

    </section>

    <!-- Sezione copyrights -->

    <section id="copyrights">
      <div>
        <span>Enjoy the low price. We are tracking any intention of piracy</span>
      </div>

      <div>
        <font-awesome-icon icon="fa-regular fa-copyright" />
        <span>2020 NEXGEN is Proudly Powered by <a href="#">Codings</a>.</span>
      </div>
    </section>

  </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

// Regole footer

footer {
  background-image: url('../assets/img/bg-10.jpg');
  background-position: center;

  // Regole sezione informazioni 

  #information {
    display: flex;
    justify-content: space-between;
    padding: 30px;
    width: 90%;
    margin: 0 auto;
    padding-top: 60px;

    #contact,
    #about,
    #transport,
    #support {
      width: calc(100% / 4 - 15px);
    }

    #about,
    #transport,
    #support {
      border-radius: 10px;
      padding: 20px 50px;
      background-color: rgba(255, 255, 255, 0.2);
    }

    ul {

      li {
        margin: 20px 0;

        a {
          padding: 10px;
        }
      }
    }

    h2 {
      color: white;
    }

    // Regole sezione contatti

    #contact {
      color: white;

      h2 {
        display: inline-block;
      }

      #background {
        display: inline-block;
        background-color: rgba(4, 131, 131, 0.4);
        border-top-left-radius: 5px;
        border-bottom-left-radius: 5px;
        padding: 3px;
        padding-left: 20px;

        h2 {
          color: $primary;
        }
      }

      p {
        margin: 20px 0;
      }

      ul {
        li {
          margin: 10px 5px;

          span {
            margin-left: 10px;
          }
        }
      }

      button {
        margin-top: 20px;
        background-color: transparent;
      }
    }
  }

  // Regole sezione copyrights

  #copyrights {
    display: flex;
    justify-content: space-evenly;
    padding: 20px 0 10px;
    background-color: rgb(33, 51, 62);
    color: white;

    span {
      margin-left: 10px;
    }

    a {
      color: $primary;
    }
  }
}
</style>
