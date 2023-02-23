<template>
  <div class="wrapper">
    <div class="content_container">
      <p class="para_content">Verschiedene Arten von Spanndecken</p>
      <h2 class="heading_content">
        Es gibt unterschiedliche Arten von Spanndecken:
      </h2>
    </div>
    <div class="images_container">
      <div class="first_thumbnail">
        <div class="first_list">
          <ul>
            <li>matt, seidenmatt oder Hochglanz-Spanndecken</li>
            <li>bedruckte Spanndecken</li>
          </ul>
        </div>
        <div class="ceiling_buttons">
          <button @click="bookFreeOffer">Kostenloses Angebot</button>
        </div>

        <div class="second_list">
          <ul>
            <li>Lichtdecken</li>
            <li>Spanndecken-Kombinationen</li>
            <li>3D oder mehrstufige Spanndecken</li>
          </ul>
        </div>

        <img src="../assets/ceilingTypes.jpg" alt="" />
      </div>

      <div class="second_thumbnail">
        <div class="fabric_list">
          <ul>
            <li>Gewebe-Spanndecken (matt oder seidenmatt)</li>
            <li>Licht-Gewebe-Spanndecken</li>
            <li>bedruckte Gewebe-Spanndecken</li>
          </ul>
        </div>
        <div class="ceiling_buttons">
          <button @click="toFabricCeiling">Kostenloses Angebot</button>
        </div>
        <img src="../assets/ceilingTypes.jpg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TypesOfCeiling",
  data() {
    return {};
  },
  methods: {
    freeOffer() {},
    toFabricCeiling() {},
  },
};
</script>

<style scoped>

/* overall wrappper */
.wrapper {
  margin: auto;
  padding: auto;
  display: flex;
  max-width: 138.4rem;
  flex-wrap: wrap;
  justify-content: center;
  padding-bottom: 20.6rem;
  background-color: var(--basic-200);
  flex-direction: column;
}

/* main container */
.content_container {
  margin-top: 13.1rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* paragraph setting */

.para_content {
  font-size: 1.5rem;
  line-height: 1.33;
  text-align: center;
  letter-spacing: normal;
  color: var(--primary-900);
}

/* heading styling */
.heading_content {
  width: 50.4rem;
  height: 8.0rem;
  font-size: 3.2rem;
  font-weight: bold;
  line-height: 1.25;
  letter-spacing: normal;
  text-align: center;
  color: var(--primary-500);
}

/* main image container setting */
.images_container {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  align-items: center;
  margin-top: 3.8rem;
  position: relative;
}

/* Thumbnail setting */
.first_thumbnail {
  position: relative;
  display: flex;
  justify-content: space-between;
  margin-bottom: 2.1rem;
}

/* Lis and List items styling */

.first_list {
  position: absolute;
  left: 5%;
  top: 5%;
  margin-left: 4.7rem;
  width: 26.3rem;
}
.first_list ul li {
  font-size: 1.5rem;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--basic-100);
}
.second_list {
  position: absolute;
  left: 40%;
  top: 5%;
  margin-left: 8.7rem;
}
.second_list ul li {
  font-size: 1.5rem;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--basic-100);
}
.fabric_list {
  position: absolute;
  left: 5%;
  top: 5%;
  margin-left: 4.7rem;
}
.fabric_list ul li {
  font-size: 1.5rem;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--basic-100);
}
/* image styling */
.first_thumbnail img {
  width: 75rem;
  height: 19.2rem;
  opacity: 0.55;
  background-blend-mode: multiply;
  background-image: linear-gradient(to bottom, #000, #000);
}

.second_thumbnail img {
  width: 75rem;
  height: 19.2rem;
  opacity: 0.55;
  background-blend-mode: multiply;
  background-image: linear-gradient(to bottom, #000, #000);
}
/* position of the pic */
.second_thumbnail {
  position: relative;
}
/* button div styling */
.ceiling_buttons {
  margin-top: 14rem;
  position: absolute;
  margin-left: 6rem;
}
/* button stext styling */
.ceiling_buttons button {
  width: 27.4rem;
  height: 3.2rem;
  border: none;
  padding: 0.8rem 1.6rem;
  border-radius: 0.4rem;
  border: solid 1px var(--primary-500);
  font-size: 1.5rem;
  line-height: 1.33;
  letter-spacing: normal;
  color: var(--primary-500);
  text-align: center;
  font-weight: bold;
  cursor: pointer;
}

</style>
