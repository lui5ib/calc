<template>
  <div>
      <nav>
        <img src="" alt="">
        <button id="button-nav">Proyecto</button>
        <button id="button-nav">Servicios</button>
        <button id="button-nav">Iniciar sesión</button>
      </nav>
    </div>
      <body>
      <div class="container">
          <form class="square">
              <label for="papel">Papel:</label>
              <input type="text" id="papel" placeholder="Tipo de papel">

              <label for="precio">Precio:</label>
              <input type="text" id="precio" placeholder="Precio por unidad">

              <label for="cantidad">Cantidad:</label>
              <input type="text" id="cantidad" placeholder="Cantidad">

              <label for="accion">Acción:</label>
              <select id="accion">
                  <option value="compra">Compra</option>
                  <option value="venta">Venta</option>
              </select>

              <button class="calculate-button">Calcular</button>
          </form>
      </div>
</body>
</template>

<script setup>

</script>

<style>
* {
  background-color: black;
}

#button-nav {
  border-color: orange;
  border-width: 3px;
  text-decoration: none;
  color: white;
}
#box {
  border-color: orange;
  border-width: 3px;
  text-decoration: none;
  color: white;
  display:block;
  position: absolute;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f2f2f2;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.container {
    text-align: center;
}

.square {
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
}

label, input, select {
    display: block;
    margin: 10px 0;
}

input, select {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

.calculate-button {
    background-color: orange;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
}

.calculate-button:hover {
    background-color: darkorange;
}

</style>