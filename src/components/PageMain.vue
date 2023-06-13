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

      // Regole generali dei componenti della sezione

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

}


</style>
