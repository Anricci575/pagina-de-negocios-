<template>
  <article class="card">
    <img :src="product.img" :alt="product.title" />
    <div style="display:flex;justify-content:space-between;align-items:center">
      <h3 style="margin:0;font-size:1rem">{{ product.title }}</h3>
      <div class="price">{{ product.price }}</div>
    </div>
    <p class="small" style="margin:0">{{ product.desc }}</p>
    <div style="margin-top:8px;display:flex;gap:8px">
      <button class="btn" @click="buy">Comprar</button>
      <button class="btn" style="background:#e6eef6;color:var(--primary)" @click="more">Ver</button>
    </div>
  </article>
</template>

<script>
export default {
  name: 'ProductCard',
  props: ['product'],
  methods: {
    buy() {
      alert(`Añadido al carrito: ${this.product.title}`)
    },
    more() {
      alert(`Más información de: ${this.product.title}`)
    }
  }
}
</script>