<template>
    <div class="wrapper">
      <div class="container">
        <h2>Spanndecken-Montage vom Profi</h2>
        <div class="carousel-frame">
          <transition-group name="fade">
            <div v-for="i in [currentIndex]" :key="i">
              <img :src="currentImg" />
            </div>
          </transition-group>
          <div class="arrow-btn">
            <div>
              <button class="prev" @click="prev">
                <img src="../assets/27-icon-arrow-left.svg" alt="" />
              </button>
            </div>
            <div>
              <button class="next" @click="next">
                <img src="../assets/27-icon-arrow-right.svg" alt="" />
              </button>
            </div>
          </div>
        </div>
  
        <div class="description">
          <p>
            Herzlich Willkommen bei Spanndecken Markowski. Wir sind Ihr
            Spezialist, wenn es um die Spanndecken-Montage geht. Ob Spanndecken,
            <br /><br>
            Lackspanndecken oder Lichtdecken: Diese Art der Deckengestaltung ist
            beliebt und sorgt für einen Blickfang in jedem Raum. Doch die Montage
            ist nicht in jedem Fall leicht umzusetzen.<br /><br> Aus diesem Grund hat sich
            die Firma Markowski auf die Spanndecken-Montage spezialisiert. <br /><br>
            Gemeinsam mit unseren qualifizierten Mitarbeitern ermöglichen wir
            Ihnen, Ihre Wünsche in die Tat umzusetzen. Aufgrund langjähriger
            Erfahrung können wir Sie auch bei der Planung rund um die
            Deckenrenovierung beraten.
          </p>
          <div class="buttons">
            <button class="request_button">
              <a href="">Gratis Beratung anfordern</a>
            </button>
            <button class="offer_button">
              <a href="">Individuelles angebot</a>
            </button>
          </div>
        </div>
      </div>
    </div>
  </template>
  <script>
  export default {
    name: "CarouselCard",
    data() {
      return {
        images: [
          require("@/assets/img3.jpg"),
          require("@/assets/img1.jpg"),
          require("@/assets/img2.jpg"),
          require("@/assets/img4.jpg"),
          require("@/assets/img5.jpg"),
   
        ],
        timer: null,
        currentIndex: 0,
      };
    },
  
    mounted: function () {
      this.startSlide();
    },
  
    methods: {
      startSlide: function () {
        this.timer = setInterval(this.next, 100000);
      },
  
      next: function () {
        this.currentIndex += 1;
      },
      prev: function () {
        this.currentIndex -= 1;
      },
    },
  
    computed: {
      currentImg: function () {
        return this.images[Math.abs(this.currentIndex) % this.images.length];
      },
    },
  };
  </script>
  <style>
  /* Main Wrapper style */
  .wrapper {
    width: 144rem;
    height: 94.8rem;
    background-color: var(--basic-200);
    margin: auto;
    position: relative;
  }
  
  /* Heading Style */
  
  h2 {
    width: 76.1rem;
    height: 5.6rem;
    font-weight: 700;
    font-size: 4.6rem;
    font-weight: bold;
    line-height: 1.22;
    margin-right: 36.4rem;
    margin-left: 31.5rem;
    margin-top: 9.7rem;
    position: absolute;
    color: var(--primary-900);
  }
  
  /* Container of carousel and description */
  
  .container {
    display: flex;
  }
  /* Carousel frame with image */
  
  .carousel-frame {
    margin-top: 26.17rem;
    width: 50%;
    margin-left: 15rem;
    position: relative;
  }
  .carousel-frame img {
    width: 55.5rem;
    height: 52.7rem;
  }
  
  
  
  /* Arrow button div */
  
  .arrow-btn {
    position: absolute;
    top: 80%;
    display: flex;
    left: 35%;
    transform: translate(-50%, -50%);
    -ms-transform: translate(-50%, -50%);
    text-align: center;
    padding-bottom: 5.27rem;
    position: fixed;
  }
  .prev {
    width: 5.6rem;
    height: 5.6rem;
    border-radius: 0.44rem;
    border: 0;
  
    background-color:var(--basic-200);
  }
  .prev img {
    width: 2.4rem;
    height: 2.4rem;
  }
  .next {
    width: 5.6rem;
    height: 5.6rem;
    border-radius: 0.44rem;
    border: 0;
   
    background-color: var(--primary-500);
  }
  .next img {
    width: 2.4rem;
    height: 2.4rem;
  }
  
  /* Description box */
  
  .description {
    margin-top: 26.17rem;
    width: 50%;
  }
  .description p {
    width: 45.8rem;
    height: 33.6rem;
    font-size: 15px;
    font-weight: bold;
    line-height: 1.6;
    margin-left: 12.7rem;
    margin-right: 15rem;
    letter-spacing: normal;
    color: var(--primary-600);
  }
  
  /* link Buttons */
  
  .buttons {
    margin-top: 2.8rem;
  }
  
  .buttons a {
    text-decoration: none;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 2px;
  }
  .request_button,
  .offer_button {
    width: 37.5rem;
    height: 5.6rem;
    padding: 1.6rem 2.4rem;
    border-radius: 0.4rem;
    border: solid 1px var(--primary-500);
    margin-left: 12.7rem;
    margin-right: 15rem;
  }
  
  .offer_button {
    margin-top: 1.4rem;
    background-color: var(--primary-500);
  }
  
  .offer_button a {
    width: 32.7rem;
    height: 2.4rem;
    font-size: 1.8rem;
    font-weight: bold;
    line-height: 1.33;
    letter-spacing: normal;
    text-align: center;
    color: var(--basic-100);
  }
  .request_button a {
    width: 32.7rem;
    height: 2.4rem;
    font-size: 1.8rem;
    font-weight: bold;
    line-height: 1.33;
    letter-spacing: normal;
    text-align: center;
    color: var(--primary-500);
  }
  
  /* For Responsiveness */
  
  .column {
    flex: 33.33%;
    padding: 5px;
  }
  
  .row {
    display: flex;
  }
  .request_button {
    background-color: #d0dcd6;
  }
  
  /* Transition Group style */
  
  .fade-enter-active,
  .fade-leave-active {
    transition: all 0.5s ease;
    overflow: hidden;
    visibility: visible;
    position: absolute;
    width: 100%;
    opacity: 1;
  }
  
  .fade-enter,
  .fade-leave-to {
  
    width: 100%;
    opacity: 0;
    
  }
  
  
  
  /* MEDIA QUERY FOR 1330px */
  
  @media (max-width: 83em) {
    .container{
      flex-direction: column;
      align-content: center;
      flex-wrap: wrap;
    }
   .wrapper{
    width: 100%;
    height: 100%;
   }
   .description{
    margin-left: 3em;
    width:50%;
    height: 100%;
    margin-top: 1em;
   }
   .arrow-btn{
    left: 52%;
    top: 79%;
   }
   .description p{
    margin-left: 5rem;
    height: 100%;
   }
  }
  </style>