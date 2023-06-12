<script>

export default {
    name: "PageHeader",
    data() {
      return {
        workHours: {
          firstDay : 'Mon',
          lastDay : 'Sat',
          openingtime : '09:00',
          closingTime : '18:00'
        },
        contacts: [
        {
          stateCode: '1',
          areaCode: '305',
          phoneNumber: '12345678'
        },
        {
          mail: 'hello@exemple.com'
        }
        ]
      }
    }
}
</script>

<template>

<header>
  <section id="info">

    <!-- infomrazioni orario di lavoro -->

    <div id="work-time">
      <font-awesome-icon icon="fa-solid fa-clock" />
      <span>Open Hours: {{workHours.firstDay}} - {{workHours.lastDay}} - {{workHours.openingtime}} - {{workHours.closingTime}}</span>
    </div>

    <!-- Informazioni contatti aziendali -->

    <div id="contacts">

     <div id="mail-phone">
      
        <!-- Telefono aziendale -->

       <font-awesome-icon icon="fa-solid fa-phone" />
        <span id="phone"> +{{ contacts[0].stateCode }} 
          <span v-if="contacts[0].areaCode">({{ contacts[0].areaCode }})</span>
          {{ contacts[0].phoneNumber }}
        </span>

        <!-- Mail aziendale -->

        <font-awesome-icon icon="fa-solid fa-envelope" />
        <span id="mail"> {{contacts[1].mail}} </span>

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

  <section id="jumbotrone">
    prova
  </section>

</header>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables.scss' as *;

// Regole header

header {
  height: 500px;

  // Regole info

  #info{
    display: flex;
    padding: 15px 0;
    justify-content:space-evenly;
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
    overflow: hidden;
    background-size: cover;
    background-position: top;
  }
}

</style>
