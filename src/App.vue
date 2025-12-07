<template>
  <div>
    <Header />
    <main class="container">
      <section class="hero">
        <div class="container">
          <h1>Tu Tienda de Tecnología</h1>
          <p>Los mejores dispositivos y accesorios al mejor precio. Garantía y envío rápido.</p>
        </div>
      </section>

      <section>
        <h2>Productos destacados</h2>
        <div class="grid">
          <ProductCard
            v-for="product in products"
            :key="product.id"
            :product="product"
          />
        </div>
      </section>

      <section style="margin-top:28px;">
        <h2>Contacto</h2>
        <p class="small">¿Tienes una pregunta? Escríbenos y te responderemos pronto.</p>
        <ContactForm />
      </section>
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import ProductCard from './components/ProductCard.vue'
import ContactForm from './components/ContactForm.vue'

export default {
  components: { Header, Footer, ProductCard, ContactForm },
  data() {
    return {
      products: [
        {
          id: 1,
          title: 'Portátil Gamer X200',
          price: '€1,299',
          img: '/src/assets/placeholder-product-1.jpg',
          desc: '16GB RAM • 1TB SSD • RTX 4070'
        },
        {
          id: 2,
          title: 'Smartphone Alpha S',
          price: '€799',
          img: '/src/assets/placeholder-product-2.jpg',
          desc: 'Pantalla OLED • 128GB • Cámara 50MP'
        },
        {
          id: 3,
          title: 'Auriculares Wireless Pro',
          price: '€149',
          img: '/src/assets/placeholder-product-3.jpg',
          desc: 'Cancelación de ruido • 30h batería'
        }
      ]
    }
  }
}
</script>