<script>

export default {
    name: "PageMain",
}
</script>

<template>

<main>

  <!-- Sezione loistica -->

  <section id="logistics">

    <!-- Sezione descrizione business -->

    <div id="business-description">
      
      <!-- Sezione descrizione generale -->

      <div id="general-description">
        <h5>OUR BUSINESS AREAS</h5>
        <h2>LOGISTIC SERVICES</h2>
        <p>We are leaders in providing logistics services with a set of cutting edge technology and a team of experienced and renowned professionels.</p>

        <div id="tags">
          <button type="button">Tradition</button>
          <button type="button">Quality</button>
          <button type="button">Security</button>
        </div>

        <button type="button">READ MORE</button>
      </div>

      <!-- Sezione descrizione tecnologie -->

      <div id="technology-description">

        <div class="explicative-image">
          <img src="../assets/img/gallery-3.jpg" alt="Tecnology image">
        </div>

        <div class="description">

          <h2>Technology</h2>

          <p>Focused on developing technology solutions adapted to our client's needs.</p>

        </div>

      </div>

      <!-- Sezione descrizione trasporto -->

      <div id="transport-description">
        <div class="explicative-image">
          <img src="../assets/img/gallery-5.jpg" alt="Tecnology image">
        </div>

        <div class="description">

          <h2>Technology</h2>

          <p>Focused on developing technology solutions adapted to our client's needs.</p>

        </div>
      </div>

    </div>

  </section>

  <!-- Sezione about network -->

  <section id="about-network">
    
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

</main>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables.scss' as *;

main {

  // Regole sezione logistica
  
  #logistics {
    background-color: $mainbackground;

    // Regole sezione descrizione del business

    #business-description {
      display: flex;
      width: 80%;
      margin: 0 auto;

      // Regole comuni dei componenti della sezione

      #general-description, #technology-description, #transport-description {
        margin: 60px 0;
        width: calc(100% / 3 - 20px);
        margin-right: 20px;
      }

      // Regole sezione descrizione generale

      #general-description {
        h5 {
          color: $primary;
        }

        // Regole comuni dei componenti della sezione

        h5, h2, p, #tags {
          margin-bottom: 30px;
        }

        // Regole tags

        #tags {

          button {
            color: $primary;
            margin-right: 20px;
            background-color: rgba(204, 227, 222, .4);
            border: none;
          }
        }
      }

      // Regole immagine descrittiva
      .explicative-image {
        width: 50%;
        margin: 30px auto 0;

        img {
          width: 100%;
        }
      }

      // Regole descrizione
      .description {
        width: 50%;
        margin: 30px auto;
      }

      // Regole sezione descrizione teconologie e trasporto

      #technology-description, #transport-description {
        background-color: white; 
        border-radius: 10px;      
      }
    }
  }

  // Regole sezione about network

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

      h5, #name, p {
        margin-bottom: 30px;
      }

      h5 {
        color: $primary;
      }

      #name {
          display: flex;

          #background {
            display: inline-block;
            background-color: rgba(4, 131, 131, 0.4);
            padding: 0 5px;

            h2 {
              color: $primary;
            }
          }
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

}

</style>
