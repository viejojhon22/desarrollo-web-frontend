<template>
  <div class="container">
    {{nombre}}
      <ul>
        <li v-for="item in clientes" :key="item.id">
            {{item.nombre}}
        </li>
      </ul>
      <input type="text" v-model="nombre">
      <br>
      <a v-bind:href="url">{{url}}</a>
      <p/>
      <button @click='metodo1'>Ejecutar metodo</button>
      <p></p>

      <h1>Ejercicio 1</h1>
      <p></p>
      <input type="number" v-model="numero1">
      <input type="number" v-model="numero2">
      <p></p>
      <button @click="sumar">Sumar +</button>
      <p></p>
      <h3>Resultado {{resultado}}</h3>

      <p></p>
      <h1>Ejercicio 2</h1>
      <input type="text" v-model="tarea"/>
     
      <button @click="agregarTarea">Agregar tarea</button>
      <h5>Listado de tareas</h5>
       <ul>
        <li v-for="item in tareas" :key="item">
            {{item}}
        </li>
      </ul>
  </div> 
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data () {
    return {
      nombre : 'Alex',
      mostrar : true,
      clientes : [{id:1, nombre : 'Diego'},{id:2, nombre : 'Jonathan'}],
      url : 'https://www.google.com',
      numero1 : 0,
      numero2 : 0,
      resultado : 0,
      tarea : null,
      tareas : ['descripcion']
    }
  },
  methods : {
    metodo1 () {
        alert("Click")
    },
    sumar () {
      this.resultado = this.numero1+this.numero2
    },
    agregarTarea () {
      alert("agregar tarea "+ this.tarea)
      this.tareas.push(this.tarea)
    }
  }
}
</script>

<style scoped>
li {
  color: blue;
  font-size: 34px;
}
</style>