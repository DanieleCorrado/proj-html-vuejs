<script>

export default {
  name: "PageMain",

  data() {
    return {
      userName: '',
      userEmail: '',
      subscribers: []
    }
  },
  methods: {
    subscribe(e) {

      e.preventDefault();
      this.subscribers.push({
        name: this.userName,
        email: this.userEmail
      })
      this.userEmail = '';
      this.userName = ''
      console.log(this.subscribers)

    }
  },
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
          <p>We are leaders in providing logistics services with a set of cutting edge technology and a team of
            experienced and renowned professionels.</p>

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

    <!-- Sezione applicativi -->

    <section id="application">

      <div class="app-logo">
        <img src="../assets/img/logo-5.png" alt="Logo LESS">
      </div>

      <div class="app-logo">
        <img src="../assets/img/logo-1.png" alt="Logo Woocommerce">
      </div>

      <div class="app-logo">
        <img src="../assets/img/logo-2.png" alt="Logo Woocommerce">
      </div>

      <div class="app-logo">
        <img src="../assets/img/logo-3.png" alt="Logo Woocommerce">
      </div>

      <div class="app-logo">
        <img src="../assets/img/logo-4.png" alt="Logo Woocommerce">
      </div>

      <div class="app-logo">
        <img src="../assets/img/logo-5.png" alt="Logo LESS">
      </div>
    </section>

    <!-- Sezione news -->

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

    <!-- Sezione newsletter -->

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
          <input type="text" id="name" placeholder="Name" v-model="userName">
          <input type="email" id="name" placeholder="Email" v-model="userEmail">
          <button type="submit">SUBSCRIBE</button>
        </form>
      </div>

    </section>

  </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

main {
  background-color: $mainbackground;

  // Regole background nome sezione

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

  // Regole sezione logistica

  #logistics {

    // Regole sezione descrizione del business

    #business-description {
      display: flex;
      width: 80%;
      margin: 0 auto;

      // Regole comuni dei componenti della sezione

      #general-description,
      #technology-description,
      #transport-description {
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

        h5,
        h2,
        p,
        #tags {
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

      #technology-description,
      #transport-description {
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

  // Regole sezione applicativi

  #application {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 80%;
    margin: 0 auto;

    // Regole logo
    .app-logo {
      padding: 60px 0;
      width: calc(100% / 6);
      text-align: center;
    }
  }

  // Regole sezione news

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

  // Regole sezione newsletter

  #newsletter {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    padding-top: 50px;
    height: 400px;
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

    // Regole form newsletter

    #newsletter-form {

      #subscription {
        input {
          width: 300px;
          padding: 10px;
          filter: opacity(0.7);
          margin-bottom: 20px;
          border-radius: 5px;
          border: none;
        }
      }
    }

  }

}
</style>
