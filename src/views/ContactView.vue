<script setup lang="ts">
import { ref } from 'vue'

const name = ref('')
const message = ref('')

const sendWhatsApp = () => {
  const phoneNumber = '6285174254323'
  const text = `Halo Aricand's Cake, saya ${name.value}. ${message.value}`
  const encodedText = encodeURIComponent(text)
  const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodedText}`

  window.open(whatsappUrl, '_blank')
}
</script>

<template>
  <div class="contact-page">
    <main class="contact-content">
      <h1>Hubungi Kami</h1>
      <p class="contact-intro">
        Punya pertanyaan atau ingin melakukan pemesanan khusus? Silakan hubungi kami melalui
        formulir di bawah ini.
      </p>

      <form @submit.prevent="sendWhatsApp" class="contact-form">
        <div class="form-group">
          <label for="name">Nama Anda</label>
          <input
            type="text"
            id="name"
            v-model="name"
            placeholder="Masukkan nama lengkap"
            required
          />
        </div>

        <div class="form-group">
          <label for="message">Pesan</label>
          <textarea
            id="message"
            v-model="message"
            placeholder="Tuliskan pesan atau pesanan Anda di sini..."
            rows="5"
            required
          ></textarea>
        </div>

        <button type="submit" class="submit-btn">Kirim ke WhatsApp</button>
      </form>
    </main>
  </div>
</template>
