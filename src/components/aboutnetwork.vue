<script>

export default {
  name: 'aboutnetwork'
}
</script>

<template>
  <section id="about-network">

    <!-- Descrizione sezione -->

    <div id="network-description">

      <h5>ABOUT THE NETWORK</h5>

      <div id="name">
        <div id="background">
          <h2>The</h2>
        </div>
        <H2>Company</H2>
      </div>

      <!-- desrizione azienda -->

      <p>With all of this expertise and capability comes an unrivalled commitment to customer service.</p>

      <!-- Capacità aziendali -->

      <ul>
        <li>

          <!-- Visualizzazione percentuale -->

          <div class="radialProgressBar">
            <div class="overlay"><span class="prc-number">0</span>%</div>
          </div>

          <div class="information">
            <h2>Leadership</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>

        </li>

        <li>

          <!-- Visualizzazione percentuale -->

          <div class="radialProgressBar">
            <div class="overlay"><span class="prc-number">0</span>%</div>
          </div>

          <div class="information">
            <h2>Psychology</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>

        </li>

        <li>

          <!-- Visualizzazione percentuale -->

          <div class="radialProgressBar progress-1">
            <div class="overlay"><span class="prc-number">1</span>%</div>
          </div>

          <div class="information">
            <h2>Flexibility</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>

        </li>

      </ul>

    </div>

  </section>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables.scss' as *;

#about-network {
  background-color: black;
  background-image: url(../assets/img/about-5.jpg);
  background-repeat: no-repeat;
  background-position: right;
  background-size: contain;
  padding: 20px 0;

  // Regole descrizione network

  #network-description {
    width: 50%;
    margin: 0 40px;
    color: white;

    // Regole comuni dei componenti della sezione

    h5,
    #name,
    p {
      margin-bottom: 30px;
    }

    h5 {
      color: $primary;
    }

    ul {
      li {
        display: flex;
        align-items: center;

        // Regole cerchio percentuale
        .radialProgressBar {
          border-radius: 50%;
          width: 100px;
          height: 100px;
          display: flex;
          background: rgb(35, 35, 40);
          margin: 20px;
        }

        .radialProgressBar .overlay {
          border-radius: 50%;
          width: 80px;
          height: 80px;
          margin: auto;
          background: black;
          text-align: center;
          padding-top: 25%;
        }

        .overlay {

          .prc-number {
            font-size: 30px;
          }
        }

        .progress-1 {
          background-image: linear-gradient(0deg, #232328 50%, transparent 50%), linear-gradient(3.6deg, $primary 50%, #232328 50%);
        }

        // Regole informazioni
        .information {
          margin-top: 20px;
        }
      }
    }

  }
}
</style>