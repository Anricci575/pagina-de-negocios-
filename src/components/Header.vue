<template>
  <header class="header">
    <div class="container">
      <div class="brand">
        <img :src="logo" alt="Logo" />
        <div>
          <div>Tu Tienda Tech</div>
          <div style="font-size:0.85rem;color:rgba(255,255,255,0.85);font-weight:500">Tecnología al alcance</div>
        </div>
      </div>
      <nav>
        <a href="#productos">Productos</a>
        <a href="#contacto">Contacto</a>
        <a href="#ofertas">Ofertas</a>
      </nav>
    </div>
  </header>
</template>

<script>
import logo from '../assets/logo-placeholder.png' // ajusta ../ según la ubicación real
export default {
  data() { return { logo } }
}
</script>