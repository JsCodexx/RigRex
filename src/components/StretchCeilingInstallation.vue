<template>
  <div class="wrapper">
    <div class="main_heading"><h1>Der Einbau einer Spanndecke</h1></div>
    <div class="container">
      <div class="description">
        <p>
          Spanndecken können auch problemlos in der Küche oder im Badezimmer
          eingebaut werden Die Besonderheit liegt vor allem an der Beständigkeit
          gegenüber Feuchtigkeit. Die aufsteigende Luftfeuchtigkeit im Bad oder
          in der Küche kann durch die Spanndecken entweichen, sodass der Einsatz
          auch in Nassräumen sich an Beliebtheit erfreut. Zudem sind sie leicht
          zu reinigen und können jederzeit neu gestrichen werden.
        </p>
      </div>
      <div class="methods">
        <p>
          Der Einbau von Spanndecken ist in der Regel in jedem Raum und bei
          jeder Deckenbeschaffenheit möglich:
        </p>
        <ul>
          <li>Holzdecken</li>
          <li>Putzdecken</li>
          <li>Gipskartondecken</li>
          <li>Styropordecken</li>
          <li>Betondecken</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "StretchCeilingInstallation",
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
  background-color: var(--basic-100);
  padding-top: 15.6rem;
  padding-bottom: 15.4rem;
  max-width: 138.4rem;
}
.main_heading {
  margin-left: 15rem;
}
.main_heading h1 {
  font-size: 3.6rem;
  font-weight: bold;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--primary-900);
}
.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
.description {
  margin-left: 15rem;
  width: 40%;
  justify-content: center;
  align-items: center;
}
.description p {
  font-size: 1.5rem;
  font-weight: bold;
  margin-top: 5.7rem;
  line-height: 1.6;
  letter-spacing: normal;
  color: var(--primary-900);
}

.methods {
  margin-right: 15rem;
  margin-top: 5.7rem;
  width: 40%;
}
.methods p {
  font-size: 1.5rem;
  font-weight: bold;
  line-height: 1.6;
  letter-spacing: normal;
  color: var(--primary-500);
  padding-left: 12.5rem;
}

.methods ul {
  margin-left: 15rem;
  justify-content: center;
  padding-top: 0.4rem;
 
}

.methods ul li {
  font-size: 1.5rem;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--primary-900);
}

/* media Query at 1000px */
@media only screen and (max-width: 60em) {
  .container {
    margin: 0;
    padding: 0;
    flex-wrap: wrap;
    flex-direction: column;
    align-items: center;
  }
  .description{
    margin: 0;
    padding: 0;
    width: 90%;
  }
  .methods {
    margin-top: 2em;
    padding: 0;
    margin-right: 0;
    width: 90%;


  }
  .methods p {
    margin: 0;
    /* padding-left: 10em; */
  }
  .methods li {
    margin-top: 1em;
    margin-left: 0;
    padding: 0;
    align-items: center;
  }
}
</style>
