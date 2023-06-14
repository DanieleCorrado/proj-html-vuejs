<script>

import contact from '../dataset/contacts.json';
import store from '../dataset/store.json';

export default {
  name: 'getInTouchSection',
  data() {
    return {
      contact,
      store
    }
  },
  methods: {
    // Aggiunge indirizzo email,nome utente, numero di telefono, altre informazioni e il messaggio all'elenco di messaggi inviati dagli utenti

    sendMessage(e) {
      e.preventDefault();
      store.messages.push({
        name: store.userName,
        email: store.userEmail,
        phone: store.userPhone,
        otherInfos: store.userOtherInfo,
        message: store.userMessage
      })

      store.userName = '';
      store.userEmail = '';
      store.userPhone = '';
      store.userOtherInfo = '';
      store.userMessage = '';
      console.log(store.messages);
    }
  }

}
</script>

<template>
  <section id="get-in-touch">

    <div id="send-message">

      <!-- Descrizione sezione -->

      <div id="message-description">
        <h5>SEND A MESSAGE</h5>

        <div id="name">
          <H2>Get in</H2>
          <div id="background">
            <h2>Touch</h2>
          </div>
        </div>

        <p>We will respond to your message as soon as possible</p>

      </div>

      <!-- Modulo invio messaggio -->

      <div id="message-form">

        <form id="send-message" v-on:submit="sendMessage">

          <div id="first-row">

            <input type="text" id="message-name" placeholder="Name" v-model="store.userName" required>
            <input type="email" id="message-email" placeholder="Email" v-model="store.userEmail" required>

          </div>

          <div id="second-row">

            <input type="tel" id="message-number" placeholder="Phone" v-model="store.userPhone" required>
            <select id="other-info" v-model="store.userOtherInfo">
              <option value="altre">altre</option>
              <option value="opzioni">opzioni</option>
            </select>

          </div>

          <div id="third-row">
            <textarea type="text" id="message-text" placeholder="Message" v-model="store.userMessage" required></textarea>
          </div>

          <button type="submit">SEND</button>

        </form>

      </div>

    </div>

    <!-- Contatti azienda -->

    <div id="contact">

      <h2>Exemple Inc.</h2>
      <p>
        Lorem ipsum dolor sit, amet consectetur adipisicing elit.
      </p>
      <p>
        Sint corporis magni ad nobis optio rerum quidem obcaecati temporibus, iusto qui quo autem labore, esse
        consequuntur quibusdam amet accusantium.
      </p>

      <!-- Lista contatti azienda -->

      <ul>

        <li>
          <div class="circle">
            <font-awesome-icon icon="fa-solid fa-phone" />
          </div>
          <span id="phone">
            +{{ contact[0].stateCode }}
            <span v-if="contact[0].areaCode">({{ contact[0].areaCode }})</span>
            {{ contact[0].phoneNumber }}
          </span>
        </li>

        <li>
          <div class="circle">
            <font-awesome-icon icon="fa-solid fa-envelope" />
          </div>
          <span id="mail"> {{ contact[1].mail }} </span>
        </li>

        <li>
          <div class="circle">
            <font-awesome-icon icon="fa-solid fa-location-dot" />
          </div>
          <span id="street">{{ contact[2].streetName }}, {{ contact[2].houseNumber }}</span>
        </li>

      </ul>

    </div>

  </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

#get-in-touch {
  width: 90%;
  margin: 0 auto;
  display: flex;
  justify-content: space-evenly;
  padding: 50px 0;

  // Regole comuni dei componenti della sezione

  #send-message,
  #contact {
    width: calc(100% / 2 - 20px);
  }

  // Regole invio messaggio

  #send-message {

    // Regole descrizione sezione

    #message-description {

      h5,
      #name,
      p {
        margin-bottom: 20px;
      }

      h5 {
        color: $primary;
      }
    }

    // Regole form messaggio

    #message-form {

      input,
      select {
        width: calc(100% / 2 - 20px)
      }

      #send-message {
        width: 100%;

        #first-row {
          width: 100%;

          #message-email {
            margin-left: 20px;
          }
        }

        #second-row {

          #other-info {
            margin-left: 20px;
          }
        }

        #third-row {
          #message-text {
            width: calc(100% - 20px);
            height: 200px;
            margin-bottom: 20px;
            background-color: rgb(250, 252, 249);
          }
        }
      }
    }
  }

  // Regole contact

  #contact {
    width: 20%;

    h2,
    p {
      margin-bottom: 30px;
    }

    // Regole lsita contatti azienda

    ul {
      li {
        margin-bottom: 20px;
        color: $primary;
        display: flex;
        align-items: center;

        .circle {
          background-color: rgba(4, 131, 131, 0.4);
          border-radius: 50%;
          padding: 15px;

          .fa-location-dot {
            font-size: 14px;
            padding: 0 3px;
          }
        }

        #phone,
        #mail,
        #street {
          margin-left: 20px;
        }
      }
    }
  }

}
</style>