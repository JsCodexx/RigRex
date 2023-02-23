<template>
  <div class="wrapper">
    <div class="main_container">
      <div class="description">
        <h1>Was ist eine Spanndecke?</h1>
        <p>
          Zu einer idealen Gestaltung gehört neben der Wandgestaltung auch die
          Erneuerung der Decke. In der Regel kann die Decke überstrichen werden,
          sodass eventuelle leichte Verfärbungen nicht mehr zu sehen sind. Doch
          sobald Risse auftreten, ist mit bloßem Streichen das Problem nicht
          behoben. Auch wenn Sie Ihre Decke abhängen oder für indirekte
          Beleuchtung sorgen wollen, gibt es eine Lösung: Spanndecken. Doch was
          genau sind Spanndecken und welche Einsatzmöglichkeiten gibt es dafür?
          Dieser Frage gehen wir hier nach und geben Ihnen einen ersten
          Überblick zum Thema. Gerne können wir Ihnen bei der Montage der
          Spanndecken auch behilflich sein. Füllen Sie dazu zunächst unser
          Angebots-Formular aus!
        </p>
      </div>
      <div class="thumbnail"><img src="../assets/download.png" alt="" /></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CeilingDefination",

  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped>
.wrapper {
  margin: 0 auto;
  padding: 0 auto;
  background-color: var(--basic-100);
  max-width: 138.4rem;
}

.main_container {
  display: flex;
  padding-bottom: 8.4rem;
  gap: 12.7rem;
  justify-content: space-evenly;
  flex-direction: row;
  padding-top: 12.6rem;
}
.description {
  width: 40%;
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  align-content: center;
}
.description h1 {
  font-size: 3.6rem;
  font-weight: bold;
  line-height: 1.33;
  letter-spacing: normal;

  color: var(--primary-500);
}

.description p {
  font-size: 1.5rem;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--primary-900);
  padding-top: 2rem;
}

.thumbnail {
  width: 45.8rem;
}
.thumbnail img {
  width: 45.8rem;
  height: 35.7rem;
  border-radius: 0.4rem;
}

@media only screen and (max-width: 76.8em) {
  .main_container {
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    row-gap: 4rem;
    align-content: center;
  }
  .description {
    width: 90%;
  }
}
</style>
