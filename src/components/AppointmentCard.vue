<template>
  <div class="wrapper">
    <div class="content">
      <h1>Wir bieten die Spanndecken-Montage …</h1>
      <p>
        … in Hilden und vielen anderen Städten in Nordrhein- Westfalen an.
        Bestellen Sie die Spanndecke direkt beim Profi und lassen Sie diese von
        uns montieren!
      </p>
      <button @click="bookAppointment">
        <a href="">Termin Vereinbaren</a>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppointmentCard",
  data() {
    return {
        
    }
  },
  methods: {
    bookAppointment() {},
  },
};
</script>

<style scoped>
.wrapper {
  margin: 0;
  padding: 0;
  background-color: var(--basic-100);
}

.content {
  padding-top: 17.7rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-bottom: 15rem;
}

.content h1 {
  font-size: 3.6rem;
  font-weight: bold;
  line-height: 1.33;
  letter-spacing: normal;
  text-align: center;
  color: var(--primary-900);
}

.content p {
  font-size: 1.5rem;
  font-weight: bold;
  line-height: 1.6;
  letter-spacing: normal;
  margin-top: 1.6rem;
  text-align: center;
  color: var(--primary-600);
}

.content button {
  width: 24.9rem;
  height: 5.6rem;
  padding: 1.6rem 2.4rem;
  border: none;
  border-radius: 0.4rem;
  background-color: var(--primary-500);
  margin-top: 7.2rem;
}
.content button a {
  font-size: 18px;
  font-weight: bold;
  line-height: 1.33;
  letter-spacing: normal;
  text-align: center;
  color: var(--basic-100);
  text-decoration: none;
}
</style>
