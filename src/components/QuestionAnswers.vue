<template>
  <div class="wrapper">
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
              <i class="close down">X</i>
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
  margin: auto;
  padding: auto;
  padding-top: 12.5rem;
  flex-wrap: wrap;
  justify-content: center;
}
.heading {
  width: 36.9rem;
  height: 11.2rem;
  display: flex;
  /* flex-wrap: wrap; */
  justify-content: start;
}
.heading h1 {
  font-size: 4.6rem;
  font-weight: bold;
  line-height: 1.22;
  letter-spacing: normal;
  color: var(--primary-900);
}

.container {
  width: 75rem;
  height: 5.4rem;
  margin: 30px 277.3px 30px 0;
  padding: 1.5rem 2.3rem 1.5rem 2.4rem;
  box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.1);
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
  border: 0.4rem solid green;
  border-radius: 50%;
  padding: 0;
  color: green;
  font-weight: bold;
}
.close {
  cursor: pointer;
  position: absolute;
  top: 50%;
  right: 0%;
  padding: 12px 16px;
  transform: translate(0%, -50%);
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
  border-width: 0 3px 3px 0;
  display: inline-block;
  padding: 3px;
}
.down {
  transform: rotate(45deg);
  -webkit-transform: rotate(45deg);
}

/* ANSWER DIV */
.answer {
  width: 75rem;
  height: auto;
  box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.1);
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
  font-size: 1.5rem;
  font-weight: bold;
  line-height: 1.6;
  letter-spacing: normal;
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
