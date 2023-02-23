<template>
  <div class="wrapper">
    <div class="main_heading">
      <h5>Wo werden hauptsächlich Spanndecken montiert?</h5>
    </div>
    <article class="side_content">
      <p>
        Diese Art der Deckenverkleidung ist oft unbekannt, da die Spanndecken
        früher nur in Hotels oder Krankenhäusern montiert wurden. Heute erhalten
        Spanndecken mehr Bedeutung in privaten und gewerblichen Bereichen wie:
      </p>
      <div class="list_container">
        <ul v-for="item in list" :key="item.id" class="list-content">
          <li>{{ item.text }}</li>
        </ul>
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
  background-color: var(--basic-200);
  display: flex;
  justify-content: center;
  margin: auto;
  padding: auto;
  padding: 15.4rem 15rem 1.7rem;
  gap: 2rem;
  padding-bottom: 1.7rem;
  max-width: 138.4rem;


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
.list_container{
    margin-top: 9rem;
}
.list-content {
  font-size: 1.5rem;
  font-weight: bold;
  line-height: 1.6;
  letter-spacing: normal;
  color: var(--primary-900);
  margin-left: 2rem;
}

li {
  margin: 0;
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
  .list-content {
    font-size: 1em;
  }
}
</style>
