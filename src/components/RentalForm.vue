<template>
   <navbar />
  <div class="container">
    <h1>Rental Mobil</h1>
    <form @submit.prevent="submitForm" class="form">
      <label for="name">Nama:</label>
      <input type="text" id="name" v-model="customerName" required><br><br>

      <label for="carType">Jenis Mobil:</label>
      <input type="text" id="carType" v-model="carType" required><br><br>

      <label for="rentalDuration">Lama Peminjaman (hari):</label>
      <input type="number" id="rentalDuration" v-model.number="rentalDuration" required><br><br>

      <button type="submit">Submit</button>
    </form>

    <div v-if="submitted" class="submission">
      <h2>Detail Pemesanan:</h2>
      <p>Nama: {{ customerName }}</p>
      <p>Jenis Mobil: {{ carType }}</p>
      <p>Lama Peminjaman: {{ rentalDuration }} hari</p>
    </div>
  </div>
  
</template>

<script setup>
import { ref } from 'vue'

const customerName = ref('');
const carType = ref('');
const rentalDuration = ref('');
const submitted = ref(false);

const submitForm = () => {
  // Validasi form sebelum disubmit
  if (customerName.value && carType.value && rentalDuration.value) {
    // Tampilkan detail pemesanan setelah submit
    submitted.value = true;
  } else {
    alert('Mohon lengkapi semua field!');
  }
};
</script>

<style scoped>
.container {
  max-width: 500px;
  margin: 0 auto;
  padding: 20px;
  border-radius: 8px;
  background-color: #f8f9fa;
}

h1 {
  text-align: center;
  color: #007bff;
}

.form {
  background-color: #000000;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

label {
  font-weight: bold;
}

input[type="text"],
input[type="number"] {
  width: 100%;
  padding: 10px;
  margin: 8px 0;
  border: 1px solid #000000;
  border-radius: 5px;
  box-sizing: border-box;
}

button {
  display: block;
  width: 100%;
  padding: 10px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.submission {
  margin-top: 20px;
  padding: 20px;
  border-radius: 8px;
  background-color: #000000;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.submission h2 {
  color: #007bff;
}
</style>
