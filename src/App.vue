<template>
  <div class="container">
    <div class="formulario">
      <h1>Titulo:</h1><textarea id="titulo" v-model="titulo"></textarea>
      <hr>
      <div>
        <label for="emoji">Emoji:</label>
        <select v-model="emoji" id="emoji">
          <option value="😊">😊</option>
          <option value="😎">😎</option>
          <option value="😍">😍</option>
        </select>
      </div>
      <hr>
      <div>
        <span>Apreciación:</span>
        <label for="regular">Regular</label>
        <input type="radio" id="regular" v-model="apreciacion" value="Regular">
        <label for="bien">Bien</label>
        <input type="radio" id="bien" v-model="apreciacion" value="Bien">
        <label for="muy-bien">Muy Bien</label>
        <input type="radio" id="muy-bien" v-model="apreciacion" value="Muy Bien">
        <label for="increible">Increíble</label>
        <input type="radio" id="increible" v-model="apreciacion" value="Increíble">
      </div>
      <hr>
      <div>
        <span>Competencias Comprendidas:</span>
        <label for="morfologia">Morfología de un componente</label>
        <input type="checkbox" id="morfologia" v-model="competencias" value="Morfología de un componente">
        <label for="directivas">Directivas</label>
        <input type="checkbox" id="directivas" v-model="competencias" value="Directivas">
        <label for="one-way">One-Way y Two-Way data binding</label>
        <input type="checkbox" id="one-way" v-model="competencias" value="One-Way y Two-Way data binding">
        <label for="estado">Estado</label>
        <input type="checkbox" id="estado" v-model="competencias" value="Estado">
        <label for="mvvm">El patrón de diseño MVVM</label>
        <input type="checkbox" id="mvvm" v-model="competencias" value="El patrón de diseño MVVM">
      </div>
      <hr>
      <div>
        <label for="opinion">Opinión:</label>
        <textarea id="opinion" v-model="opinion"></textarea>
      </div>
      <hr>
    </div>
    <div class="valores">
      <h2>Valores ingresados:</h2>
      <p>Título: {{ titulo }}</p>
      <p>Emoji: {{ emoji }}</p>
      <p>Apreciación: {{ apreciacion }}</p>
      <p>Competencias Comprendidas: {{ competencias }}</p>
      <p>Opinión: {{ opinion }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      titulo: '',
      emoji: '😊',
      apreciacion: '',
      competencias: [],
      opinion: ''
    };
  }
};
</script>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  
}

.formulario {
  flex: 1;
  padding-right: 20px; /* Espacio entre el formulario y los valores ingresados */
  background-color: black;
  color: white;
  border-radius: 20px;
  margin-left: 5px
}

.valores {
  flex: 1;
  padding-left: 20px; /* Espacio entre los valores ingresados y el formulario */
  margin-left: 10px;
  margin-right: 10px;
}

/* Estilos para los campos del formulario */
label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
  margin-left: 10px;
  margin-right: 10px;
}

input[type="radio"],
input[type="checkbox"] {
  margin-right: 10px;
  margin-left: 10px;
}

select,
input[type="radio"],
input[type="checkbox"],
textarea {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-left: 10px;
  margin-right: 10px;
}
h1, span{
  margin-left: 10px;
  margin-right: 10px;
}
</style>
