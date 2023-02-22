<template>
  <div class="wrapper">
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
        Dieser Frage gehen wir hier nach und geben Ihnen einen ersten Überblick
        zum Thema. Gerne können wir Ihnen bei der Montage der Spanndecken auch
        behilflich sein. Füllen Sie dazu zunächst unser Angebots-Formular aus!
      </p>
    </div>
    <div class="thumbnail"><img src="../assets/download.png" alt="" /></div>
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
  margin: auto;
  padding: auto;
  display: flex;
  flex-direction: row;
  gap: 12.7rem;
  background-color: var(--basic-100);
  padding-bottom: 8.4rem;
  width: 138.4rem;

}

.description {
  padding-top: 12.6rem;
  padding-left: 15rem;
}
.description h1 {
  font-size: 3.6rem;
  font-weight: bold;
  line-height: 1.33;
  letter-spacing: normal;
  /* text-align: center; */
  color: var(--primary-500);
  /* align-items: start; */
}
.description p {
  font-size: 1.5rem;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--primary-900);
  padding-top: 2rem;
}

.thumbnail {
  padding-top: 12.6rem;
  padding-right: 15.1rem;
}
.thumbnail img {
  width: 45.8rem;
  height: 35.7rem;

  border-radius: 0.4rem;
}

@media only screen and (max-width: 100em) {
  .wrapper {
    flex-wrap: wrap;
    justify-content: center;
  }
  .thumbnail {
    padding: 0;
    flex-wrap: wrap;
  }
  .thumbnail img {
    padding: 0;
    margin: 0;
  }
}
@media only screen and(min-width: 64.8em) {
  .description {
    padding: 0;
    margin: 0;
  }
}
</style>
