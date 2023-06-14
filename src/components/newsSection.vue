<script>
export default {
  name: 'newsSection'
}
</script>

<template>
  <section id="news">

    <div id="container">

      <!-- Titolo sezione -->

      <div id="title">

        <h5>OUR EDITORAL CONTENT</h5>

        <div id="name">
          <H2>Latest</H2>
          <div id="background">
            <h2>News</h2>
          </div>
        </div>
      </div>

      <!-- Descrizione sezione -->

      <div id="description">

        <p>Every week we publish content about what is best in the business world.</p>
        <button type="button">SEE ALL</button>

      </div>

      <!-- Lista articoli -->

      <div id="articles">

        <!-- Articolo -->

        <div class="article">

          <div class="article-image">
            <img src="../assets/img/news-1.jpg" alt="Immagine news">
          </div>

          <div class="news-title">
            <h2>Increase creativity is possible for everyone</h2>
          </div>
        </div>

        <!-- Articolo -->

        <div class="article">
          <div class="article-image">
            <img src="../assets/img/news-2.jpg" alt="Immagine news">
          </div>

          <div class="news-title">
            <h2>Because market research is part of the business plan</h2>
          </div>
        </div>

        <!-- Articolo -->

        <div class="article">

          <div class="article-image">
            <img src="../assets/img/news-3.jpg" alt="Immagine news">
          </div>

          <div class="news-title">
            <h2>Working from home is now a trend</h2>
          </div>

        </div>

      </div>

    </div>

  </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

#news {
  background-color: white;
  padding: 70px 0;

  // Regole container news

  #container {
    width: 80%;
    margin: 0 auto;

    // Regole comuni dei componenti della sezione

    h5,
    #name,
    #description {
      margin-bottom: 30px;
    }

    h5 {
      color: $primary;
    }

    // Regole titolo sezione

    #name {
      h2 {
        font-size: 40px;
      }
    }

    // Regole pulsante

    button {
      padding: 10px 15px;
    }

    // Regole descrizione sezione

    #description {
      display: flex;
      justify-content: space-between;
    }

    // regole conteniotore articoli

    #articles {
      display: flex;
      justify-content: space-between;

      // Regole articoli
      .article {
        width: calc(100% / 3 - 20px);
        position: relative;

        // Regole immagini articoli
        .article-image {

          img {
            width: 100%;
            border-radius: 10px;
            filter: brightness(0.5);
          }

        }

        // Regole titoli articoli
        .news-title {
          width: 70%;
          position: absolute;
          bottom: 10%;
          left: 50%;
          transform: translate(-50%);
          color: white;
          text-align: center;
        }
      }
    }
  }
}
</style>