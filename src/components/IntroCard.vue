<template>
  <div class="parent">
    <div class="child1">
      <div class="image-child">
        <img src="../assets/pic.png" alt="" />
      </div>
    </div>
    <div class="child2">
      <div class="para">
        <h2>Garantie für Spanndecken</h2>
        <p>
          Das Unternehmen Spanndecken Markowski stellt höchste Ansprüche an die
          Qualität der verwendeten Materialien und Dienstleistungen. Spanndecken
          Markowski ist von der Qualität der angebotenen Produkte überzeugt und
          gewährt eine uneingeschränkte Garantie auf Spanndecken. Der
          Brandschutz und die Sicherheit für die Gesundheit unserer Spanndecken
          wird durch entsprechende Zertifikate bestätigt. Die Garantie gilt für
          alle Arten von Produktions- und Installationsarbeiten: Festigkeit der
          Nahtverbindungen, Festigkeit der Kederbefestigung, kein Durchhängen
          der Decke sowie die Sicherheit des Erscheinungsbilds und der
          Leistungsmerkmale der Bahn. Die Garantie gilt nicht für Fälle von
          Schäden an der Decke durch den Kunden sowie durch Dritte und gilt
          nicht für Fälle wie: Beschädigung der Spanndecke mit scharfen
          Gegenständen, Fluten mit Wasser und Pflege mit Chemikalien, die nicht
          für Spanndecken geeignet sind. Wir bieten Ihnen 10 Jahre Garantie für
          den Halt der Schweißnähte und Keder. Darüber hinaus bieten wir Ihnen
          die gesetzliche Gewährleistungsfrist von 2 Jahren für die Spanndecken
          Montage und das verwendete Material an.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IntroCard",
  props: {
    msg: String,
  },
};
</script>
  <style scoped>
.parent {
  position: relative;
  margin-top: 10rem;
  margin-bottom: 10rem;
  background-color: var(--basic-200);
  width: 100%;
  height: 66.4rem;
  display: flex;
  justify-content: flex-end;
}
.child1 {
  position: absolute;
  /* border: 2px solid #999;
    height: 250px; */
  top: -4.9rem;
  left: -0.2rem;
  width: 50%;
  bottom: 5.4rem;
}
.child2 {
  /* position: absolute; */
  width: 50%;
  justify-content: flex-end;
}
.image-child {
  height: fit-content;
  margin-left: 15rem;
  margin-right: 9.4rem;
}

.image-child img {
  width: 49.1rem;
  height: 76.7rem;
  top: -4.9rem;
  left: -0.2rem;
  bottom: 5.4rem;
}

.para {
  margin-top: 11.4rem;
  margin-right: 14.9rem;
  height: 52.8rem;
  width: 55.6rem;
  justify-content: start;
  margin-bottom: 2.2rem;
}
.para h2 {
  color: var(--primary-500);

  width: 55.5rem;
  height: 4.8rem;
  /* margin-top: 2.9rem; */
  margin-bottom: 3.7rem;
  /* margin-right: 15rem; */
  font-family: Inter-Regular_;
  font-size: 3.6rem;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.33;
  letter-spacing: normal;
}
p {
  color: var(--primary-600);
  font-family: Inter-Regular_;
  font-size: 15px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.6;
  letter-spacing: normal;
  height: 52.8rem;
  width: 55.6rem;
}
</style>