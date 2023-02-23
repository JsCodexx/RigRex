<template>
  <div class="wrapper">
    <div class="main_container">
      <div class="heading">
        <h1>Häufig gestellte Fragen</h1>
      </div>
      <div v-for="(question, index) in questions" :key="index">
        <div class="container">
          <div class="questionContainer">
            <h6>{{ question.query }}</h6>
            <div class="arrow_div">
              <button @click="showDescription(index)">
                <i class="arrow down"></i>
              </button>
            </div>
          </div>
        </div>
        <transition name="fade">
          <div class="answer" v-show="selectedItemIndex === index">
            <div class="cross_div">
              <button @click="showDescription(index)">
                <i class="close down">x</i>
              </button>
            </div>
            <h6>{{ question.query }}</h6>
            <p>
              {{ question.answer }}
            </p>
          </div>
        </transition>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "QuestionAnswers",
  data() {
    return {
      showDiv: true,
      selectedItemIndex: -1,
      item: 1,

      questions: [
        {
          query: "Wie werden Spanndecken montiert?",
          answer:
            "Spanndecken lassen sich in allen Räumen in beliebigen Formen montieren – egal, ob es sich um Büros, Schwimmbäder, Sporthallen, Wohnungen, Clubs, Konzerthallen, Läden, Supermärkte, Restaurants oder Salons handelt. Auch Dachschrägen, unebenen Decken, Rundungen, Beleuchtungskörper, Belüftungsanlagen oder komplexe Grundrisse stellen kein Problem dar.",
        },
        {
          query: "Wie werden Spanndecken montiert?",
          answer:
            "Spanndecken lassen sich in allen Räumen in beliebigen Formen montieren – egal, ob es sich um Büros, Schwimmbäder, Sporthallen, Wohnungen, Clubs, Konzerthallen, Läden, Supermärkte, Restaurants oder Salons handelt. Auch Dachschrägen, unebenen Decken, Rundungen, Beleuchtungskörper, Belüftungsanlagen oder komplexe Grundrisse stellen kein Problem dar.",
        },
        {
          query: "Wie werden Spanndecken montiert?",
          answer:
            "Spanndecken lassen sich in allen Räumen in beliebigen Formen montieren – egal, ob es sich um Büros, Schwimmbäder, Sporthallen, Wohnungen, Clubs, Konzerthallen, Läden, Supermärkte, Restaurants oder Salons handelt. Auch Dachschrägen, unebenen Decken, Rundungen, Beleuchtungskörper, Belüftungsanlagen oder komplexe Grundrisse stellen kein Problem dar.",
        },
        {
          query: "Wie werden Spanndecken montiert?",
          answer:
            "Spanndecken lassen sich in allen Räumen in beliebigen Formen montieren – egal, ob es sich um Büros, Schwimmbäder, Sporthallen, Wohnungen, Clubs, Konzerthallen, Läden, Supermärkte, Restaurants oder Salons handelt. Auch Dachschrägen, unebenen Decken, Rundungen, Beleuchtungskörper, Belüftungsanlagen oder komplexe Grundrisse stellen kein Problem dar.",
        },
        {
          query: "Wie werden Spanndecken montiert?",
          answer:
            "Spanndecken lassen sich in allen Räumen in beliebigen Formen montieren – egal, ob es sich um Büros, Schwimmbäder, Sporthallen, Wohnungen, Clubs, Konzerthallen, Läden, Supermärkte, Restaurants oder Salons handelt. Auch Dachschrägen, unebenen Decken, Rundungen, Beleuchtungskörper, Belüftungsanlagen oder komplexe Grundrisse stellen kein Problem dar.",
        },
        {
          query: "Wie werden Spanndecken montiert?",
          answer:
            "Spanndecken lassen sich in allen Räumen in beliebigen Formen montieren – egal, ob es sich um Büros, Schwimmbäder, Sporthallen, Wohnungen, Clubs, Konzerthallen, Läden, Supermärkte, Restaurants oder Salons handelt. Auch Dachschrägen, unebenen Decken, Rundungen, Beleuchtungskörper, Belüftungsanlagen oder komplexe Grundrisse stellen kein Problem dar.",
        },
        {
          query: "Wie werden Spanndecken montiert?",
          answer:
            "Spanndecken lassen sich in allen Räumen in beliebigen Formen montieren – egal, ob es sich um Büros, Schwimmbäder, Sporthallen, Wohnungen, Clubs, Konzerthallen, Läden, Supermärkte, Restaurants oder Salons handelt. Auch Dachschrägen, unebenen Decken, Rundungen, Beleuchtungskörper, Belüftungsanlagen oder komplexe Grundrisse stellen kein Problem dar.",
        },
        {
          query: "Wie werden Spanndecken montiert?",
          answer:
            "Spanndecken lassen sich in allen Räumen in beliebigen Formen montieren – egal, ob es sich um Büros, Schwimmbäder, Sporthallen, Wohnungen, Clubs, Konzerthallen, Läden, Supermärkte, Restaurants oder Salons handelt. Auch Dachschrägen, unebenen Decken, Rundungen, Beleuchtungskörper, Belüftungsanlagen oder komplexe Grundrisse stellen kein Problem dar.",
        },
      ],
    };
  },
  methods: {
    showDescription(index) {
      if (this.selectedItemIndex === index) {
        // If the selected item is already open, close it
        this.selectedItemIndex = -1;
      } else {
        // Otherwise, open the selected item
        this.selectedItemIndex = index;
      }
    },
  },
};
</script>

<style scoped>
.wrapper {
  width: 138.4rem;
  height: auto;
  background-color: var(--basic-100);
  display: flex;
  flex-direction: column;
  margin: 0 auto;
  padding: 0 auto;
  align-items: center;
  padding-bottom: 12.6rem;
  flex-wrap: wrap;
}
/* main heading setting */

.heading {
  margin-top: 12.5rem;
  width: 36.9rem;
  height: 11.2rem;
  text-align: start;
}
.heading h1 {
  font-size: 4.6rem;
  font-weight: bold;
  line-height: 1.22;
  letter-spacing: normal;
  color: var(--primary-900);
  width: 36.9rem;
  height: 11.2rem;
}

/* question container */
.container {
  width: 75rem;
  height: 5.4rem;
  margin: 3.0rem 0;
  padding: 1.5rem 2.3rem 1.5rem 2.4rem;
  box-shadow: 0 .2rem .6rem 0 rgba(0, 0, 0, 0.1);
  background-color: var(--basic-100);
  justify-content: center;
  align-items: center;
  position: relative;
}

.questionContainer h6 {
  font-size: 1.8rem;
  font-weight: bold;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--primary-900);
}

/* CLOSE BUTTON */
.cross_div {
  position: absolute;
  top: 2%;
  right: 3%;
}
.cross_div i {
  border:  solid green;
  border-radius: 50%;
  padding: 0;
  margin: 0;
  color: green;  
}
.cross_div button{
  border: none;
}

/* ARROW BUTTON */

.arrow_div {
  position: absolute;
  top: 25%;
  right: 3%;
}
.arrow_div button {
  border: none;
  overflow: hidden;
  color: transparent;
  background-color: transparent;
  cursor: pointer;
}
.arrow {
  border: solid rgb(132, 131, 131);
  border-width: 0 .3rem .3rem 0;
  display: inline-block;
  padding: .3rem;
  width: 1rem;
  height: 1rem;
  /* margin: 0 0 0 35.8px; */
  object-fit: contain;
}
.down {
  transform: rotate(45deg);
  -webkit-transform: rotate(45deg);
}

/* ANSWER DIV */
.answer {
  width: 75rem;
  height: auto;
  box-shadow: 0 .2rem .6rem 0 rgba(0, 0, 0, 0.1);
  background-color: var(--basic-200);
  margin-top: 2rem;
  padding-bottom: 3.91rem;
  position: relative;
  justify-content: start;
}
.answer h6 {
  font-size: 1.8rem;
  font-weight: bold;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--primary-500);
  padding-top: 3.1rem;
  padding-bottom: 1.5rem;
}
.answer p {
  width: 55.6rem;
  height: 12.0rem;
  font-size: 1.5rem;
  font-weight: bold;
  line-height: 1.6;
  letter-spacing: normal;
  padding-left: 9.7rem;
  margin-bottom: 3.91rem;
  color: var(--primary-900);
}

/* Transitions */

.fade-enter-active,
.fade-leave-active {
  transition: all 0.3s ease-out;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
