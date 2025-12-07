<template>
  <form @submit.prevent="submit" style="max-width:720px">
    <div class="form-row">
      <input class="input" v-model="name" placeholder="Nombre" required />
      <input class="input" v-model="email" placeholder="Correo electrónico" type="email" required />
    </div>
    <div style="margin-top:8px">
      <textarea class="input" v-model="message" rows="5" placeholder="Tu mensaje" required></textarea>
    </div>
    <div style="margin-top:10px;display:flex;gap:8px;align-items:center">
      <button class="btn" type="submit">Enviar</button>
      <div class="small">Te responderemos en 24-48 horas.</div>
    </div>
  </form>
</template>

<script>
export default {
  name: 'ContactForm',
  data() {
    return {
      name: '',
      email: '',
      message: ''
    }
  },
  methods: {
    submit() {
      // Aquí podrías integrar una API o enviar a un servicio de correo.
      console.log('Contacto enviado', { name: this.name, email: this.email, message: this.message })
      alert('Gracias, hemos recibido tu mensaje. Nos pondremos en contacto pronto.')
      this.name = ''
      this.email = ''
      this.message = ''
    }
  }
}
</script>