<template>  <div class="wrapper">
    <div class="heading_container">
      <div class="heading">Was Ist eigentlich eine spanndecke?</div>
      <div class="sub_heading">Und wie wird eine Spanndecke Montiert?</div>
    </div>
    <div class="content_container">
      <div class="description_box">
        <p>
          Spanndecken bieten eine saubere und dauerhafte Lösung für Ihre
          Zimmerecke. Hier noch mehr beschreibender text, wie das im groben so
          ist und geht. <br> <br> den User abholen, der noch nicht weiß, ob er soetwas
          überhaupt will. kein vorwissen vorraussetzen. <br> <br> Lorem ipsum dolor sit
          amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor
          invidunt ut labore et dolore magna aliquyam erat. <br> <br> At vero eos et
          accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren,
          no sea takimata sanctus est Lorem ipsum dolor sit amet.
        </p>
      </div>
      <div class="video_frame">
        <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY" title="Iframe Example"></iframe>
      </div>
    </div>
  </div>
  </template>

<script>
export default {
  name: "CeilingVideo",
  props: {
    msg: String,
  },
};

</script>

<style scoped>.wrapper {
     width: 138.4rem;

    height: 82.6rem;
    background-color: var(--basic-100);
    display: flex;
    flex-wrap: wrap;

  }
  
  .heading_container {
    padding-top: 13.9rem;
    display: flex;
    flex-direction: column;
  }
  .heading {
    width: 39.2rem;
    height: 3.2rem;
    margin: 0 89.8rem 0 15rem;
    font-size: 2.2rem;
    font-weight: bold;
    line-height: 1.45;
    letter-spacing: normal;
    color: var(--primary-500);
  }
  .sub_heading {
    margin: 0 4.8rem 0 15rem;
    width: 1026px;
    height: 48px;
    font-size: 36px;
    font-weight: bold;
    line-height: 1.33;
    letter-spacing: normal;
    color: var(--primary-900);
  }
  .content_container {
    display: flex;
    width: 100%;
    justify-content: space-around;
    flex-direction: row;
  }
  .description_box {
    margin-left: 15rem;
    margin-top: 8.5rem;
    margin-bottom: 15.1rem;
    width: 48.4rem;
    height: 37.1rem;
    font-size: 1.5rem;
    font-weight: bold;
    line-height: 1.6;
    letter-spacing: normal;
    color: var(--primary-900);
  }
  .video_frame {
  
    width: 61rem;
    height: 35.7rem;
    border-radius: 0.4rem;
    margin: 8.5rem 15rem 16.5rem 4.6rem;
  }
  .video_frame iframe {
    width: 61rem;
    height: 35.7rem;
  }
  /*  */
  @media (max-width: 1330px) {
    .content_container {
      flex-direction: column;
    }
    .heading_container {
      align-content: center;
    }
  
    .video_frame {
      margin: 0;
      margin-left: 15em;
    }
    .description_box {
      width: 60em;
      height: 20em;
    }
  }</style>