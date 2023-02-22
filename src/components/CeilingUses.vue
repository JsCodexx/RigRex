<template>
  <div class="wrapper">
    <div class="thumbnail">
      <img src="../assets/download1.png" alt="" />
    </div>
    <article class="description">
      <h1>Spanndecken sind modern und vielseitig einsetzbar</h1>
      <h4>
        Spanndecken besitzen eine lange Lebensdauer, sind modern und bieten
        viele Möglichkeiten, Ihre Decke in Szene zu setzen:
      </h4>
      <ul>
        <li>Einbauspots können den Raum in ein angenehmes Licht wandeln</li>
        <li>Einbaustrahler sorgen für indirektes Licht.</li>
      </ul>
      <p>
        <br />
        Das System der Spanndecke ist simpel und kann innerhalb eines Tages von
        uns montiert werden. Mit Hilfe von Aluminiumleisten wird das
        Spanndecken-System auf der Decke montiert. Die Besonderheit dabei: die
        Montage der Spanndecke ist in der Höhe variabel. Das heißt, Sie können
        die Decke auch abhängen, um beispielsweise indirektes Licht hinter der
        Spanndecke anzubringen. Die minimale Abhang-Hoöhe beträgt ca. 3 cm.
        Diese ist allerdings vor allem von der Wahl der Beleuchtung abhängig.
        Hängelampen benötigen einen Abhang der Spanndecke um etwa 3 cm.
        Einbaustrahler hingegen brauchen etwa 8 cm Platz zwischen alter Decke
        und neuer Spanndecke.
      </p>
    </article>
  </div>
</template>

<script>
export default {
  name: "CeilingUses",
  data() {
    return {
      content: [
        {
          title: "Spanndecken sind modern und vielseitig einsetzbar",
          image:require('@/assets/download1.png'),
          use: "Spanndecken besitzen eine lange Lebensdauer, sind modern und bietenviele Möglichkeiten, Ihre Decke in Szene zu setzen",
          points: {
            1: "Einbauspots können den Raum in ein angenehmes Licht wandeln",
            2: "Einbaustrahler sorgen für indirektes Licht.",
          },
          description:
            "Das System der Spanndecke ist simpel und kann innerhalb eines Tages vonuns montiert werden. Mit Hilfe von Aluminiumleisten wird dasSpanndecken-System auf der Decke montiert. Die Besonderheit dabei: di Montage der Spanndecke ist in der Höhe variabel. Das heißt, Sie können die Decke auch abhängen, um beispielsweise indirektes Licht hinter der",
        },
      ],
    };
  },
  methods: {},
};
</script>

<style scoped>
.wrapper {
  display: flex;
  margin: auto;
  padding:auto;
  gap: 12.7rem;
  /* flex-wrap: wrap; */
  flex-direction: row;
  background-color: var(--basic-200);
  padding-bottom: 12.6rem;
  width: 138.4rem;


}
.thumbnail {
  margin-top: 10.6rem;
  border-radius: 0.4rem;
}
.thumbnail img {
  width: 50.9rem;
  height: 60.5rem;
}
.description {
  margin-top: 10.6rem;
  padding-top: 5.6rem;
  padding-right: 15rem;

  font-size: 1.5rem;

  line-height: 1.33;
  letter-spacing: normal;
  color: var(--primary-900);
}
.description h1 {
  font-size: 3.6rem;
  font-weight: bold;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--primary-900);
}
.description h4 {
  font-size: 1.5rem;
  padding-top: 6.9rem;
  font-weight: bold;
  line-height: 1.6;
  letter-spacing: normal;
  color: var(--primary-900);
}
.description ul {
  padding-top: 3.6rem;
}

@media only screen and (max-width: 90.6em) {
  .wrapper {
    flex-wrap: wrap;
    justify-content: center;
  }
  .description {
    padding: 0 3rem;
    padding-top: 0;
  }
  .thumbnail img {
    width: auto;
    height: auto;
  }
}
</style>
