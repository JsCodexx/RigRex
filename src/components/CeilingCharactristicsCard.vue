<template>
  <div class="wrapper">
    <div class="main_heading">
      <h5>Eigenschaften von Spanndecken</h5>
    </div>
    <article class="side_content">
      <p>
        Die richtige Auswahl der Art der Spanndecke hängt oft von den jeweiligen
        Eigenschaften der Spanndecke ab
      </p>
      <div class="side_para">
        <p>
          Leichte Reinigung Durch Ihre Beschichtung sind sie langlebig Lampen
          können auch danach eingebaut werden, da die Spanndecken leicht
          abnehmbar sind Farben können individuell gewählt werden Einbau auch
          bei Bewohnung der Räume möglich Spanndecken-Montage innerhalb eines
          Tages möglich Alte Decken können überspannt werden Beleuchtung,
          Gardinenschienen oder Lüftung können darauf montiert werden
        </p>
      </div>
    </article>
  </div>
</template>

<script>
import CeilinginstallationCard from "./CeilingInstallationCard.vue";
export default {
  name: CeilinginstallationCard,

  data() {
    return {
      list: [
        {
          id: "1",
          text: "Wohnungen (Wohnzimmer, Badezimmer, Flur, Küche, usw.)",
        },
        { id: "2", text: "Geschäftsräume" },
        { id: "3", text: "Büros" },
        { id: "4", text: "Fitnessstudio" },
        { id: "5", text: "Bar" },
        { id: "6", text: "Kindergarten" },
        { id: "7", text: "Arztpraxen" },
        { id: "8", text: "Banken" },
        { id: "9", text: "und vielen anderen Einrichtungen" },
      ],
    };
  },
  methods: {},
};
</script>

<style scoped>
.wrapper {
  background-color: var(--basic-100);
  display: flex;
  justify-content: center;
  margin: auto;
  padding: auto;
  padding: 15.4rem 15rem 1.7rem;
  gap: 2rem;
}

.main_heading {
  width: 50%;
  padding-right: 12rem;
  margin-top: 1rem;
  font-size: 4.6rem;
  font-weight: bold;
  line-height: 1.22;
  letter-spacing: normal;
  color: var(--primary-900);
}
.side_content {
  width: 50%;
  margin-right: 15rem;
  margin-left: 12.7rem;
  padding-top: 1rem;
  font-size: 2.2rem;
  font-weight: bold;
  line-height: 1.45;
  letter-spacing: normal;
  color: var(--primary-900);
  flex-wrap: wrap;
}
.side_para {
  margin-top: 9rem;
}
.side_para p {
  font-size: 1.5rem;
  font-weight: bold;
  line-height: 1.6;
  letter-spacing: normal;
  color: var(--primary-900);
  margin-left: 2rem;
}


/* Media query */
@media only screen and (max-width: 71.4em) {
  .wrapper {
    flex-wrap: wrap;
    font-size: small;
    margin: 0;
    padding: 0;
  }
  .main_heading {
    font-size: 3em;
  }
  .side_content {
    font-size: 1em;
  }
  .side_para {
    font-size: 1em;
  }
}
</style>
