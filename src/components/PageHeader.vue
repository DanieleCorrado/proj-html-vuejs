<script>
import contacts from '../dataset/contacts.json';

export default {
  name: "PageHeader",
  data() {
    return {
      workHours: {
        firstDay: 'Mon',
        lastDay: 'Sat',
        openingtime: '09:00',
        closingTime: '18:00'
      },
      contact: contacts,
      menuOption: [
        {
          optionName: 'HOME',
          optionLink: '#'
        },
        {
          optionName: 'SERVICES',
          optionLink: '#'
        },
        {
          optionName: 'SKILLS',
          optionLink: '#'
        },
        {
          optionName: 'PARTERS',
          optionLink: '#'
        },
        {
          optionName: 'BLOG',
          optionLink: '#'
        },
      ]
    }
  }
}
</script>

<template>
  <header>

    <!-- Sezione inforzazioni azienda -->

    <section id="info">

      <!-- infomrazioni orario di lavoro -->

      <div id="work-time">
        <font-awesome-icon icon="fa-solid fa-clock" />
        <span>Open Hours: {{ workHours.firstDay }} - {{ workHours.lastDay }} - {{ workHours.openingtime }} -
          {{ workHours.closingTime }}</span>
      </div>

      <!-- Informazioni contatti aziendali -->

      <div id="contacts">

        <div id="mail-phone">

          <!-- Telefono aziendale -->

          <font-awesome-icon icon="fa-solid fa-phone" />
          <span id="phone"> +{{ contact[0].stateCode }}
            <span v-if="contact[0].areaCode">({{ contact[0].areaCode }})</span>
            {{ contact[0].phoneNumber }}
          </span>

          <!-- Mail aziendale -->

          <font-awesome-icon icon="fa-solid fa-envelope" />
          <span id="mail"> {{ contact[1].mail }} </span>

        </div>

        <!-- Informazioni social aziendali -->

        <div id="socials">

          <!-- Facebook -->

          <a href="#">
            <font-awesome-icon icon="fa-brands fa-facebook-f" />
          </a>

          <!-- Twitter -->

          <a href="#">
            <font-awesome-icon icon="fa-brands fa-twitter" />
          </a>

          <!-- Linkedin -->

          <a href="#">
            <font-awesome-icon icon="fa-brands fa-linkedin-in" />
          </a>

        </div>

      </div>

    </section>

    <!-- Sezione call to action-->

    <section id="jumbotrone">

      <div id="top-jumbo">

        <div id="name">
          <div id="background">
            <h2>NEX</h2>

          </div>
          <H2>GEN</H2>
        </div>


        <div id="menu">

          <nav id="navigation">
            <ul>
              <li v-for="option in menuOption">
                <a :href="option.optionLink"> {{ option.optionName }}</a>
              </li>
            </ul>

          </nav>

          <button type="button"> GET IN TOUCH</button>

        </div>

      </div>

      <div id="call-to-action">

        <h1>Logistics that goes further.</h1>
        <p>For 20 years working with the most innovative in the field of transport. </p>
        <button type="button" id="get-in-touch">GET IN TOUCH</button>
        <button type="button" id="read-more">READ MORE</button>

      </div>

    </section>

  </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

// Regole header

header {
  height: 500px;

  // Regole info

  #info {
    display: flex;
    padding: 15px 0;
    justify-content: space-evenly;
    background-color: rgb(33, 51, 62);
    color: white;
    height: 10%;

    #work-time {
      span {
        margin-left: 10px;
      }
    }

    // Regole contatti

    #contacts {
      display: flex;

      #mail-phone {

        #phone {
          margin-left: 10px;
          margin-right: 40px;
        }

        #mail {
          margin-left: 10px;
        }
      }

      // Regole social

      #socials {
        margin-left: 20px;

        a {
          padding: 20px;
        }
      }
    }
  }

  #jumbotrone {
    height: 90%;
    background-image: url(../assets/img/jumbo.jpg);
    filter: brightness(.85);
    overflow: hidden;
    background-size: cover;
    background-position: bottom;
    color: white;
    position: relative;

    // Regole parte superiore del jumbotrone

    #top-jumbo {
      width: 60%;
      margin: 0 auto;
      margin-top: 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;

      #name {
        display: flex;

        #background {
          display: inline-block;
          background-color: rgba(4, 131, 131, 0.4);
          border-top-left-radius: 5px;
          border-bottom-left-radius: 5px;
          padding-left: 20px;

          h2 {
            color: $primary;
          }
        }
      }

      #menu {

        #navigation {

          display: inline-block;
          padding: 0 10px;

          ul {
            display: flex;
            list-style: none;

            li {
              a {
                padding: 10px;
              }
            }
          }
        }
      }
    }

    // Regole call to action del jumbotrone

    #call-to-action {
      width: 20%;
      position: absolute;
      top: 100px;
      left: 600px;

      h1 {
        margin-bottom: 20px;
        font-size: 50px;
      }

      p {
        margin-bottom: 30px;
        font-size: 18px;
      }

      #get-in-touch {
        margin-right: 30px;
      }

      #read-more {
        background-color: transparent;
      }
    }
  }
}
</style>
