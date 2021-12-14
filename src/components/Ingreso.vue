<template lang="html">

  <section class="scr-componentes-ingreso">
    <div class="jumbotron">
      <h1>Final NT2 - DERMISACHE, Salma</h1>
      <br>

      <label>Ingrese monto en $</label>
      <input type="number" id="pesos" v-model="pesos" name="pesos" class="form-control" />
      <br>

       <label>Ingrese valor del dolar en $</label>
      <input type="number" id="dolares" v-model="dolares" name="dolares"  class="form-control" />
      <br>

      <h4>Valor convertido en U$D: {{obtenerTotal | convertir}}</h4>

      <!-- -------------------------RESPUESTAS----------------------------- -->
       <br>
        <hr>
        <h3>RESPUESTAS</h3>

      <ol>
       
        <li value="1"> C </li>
        <li>B,C</li>
        <li>C</li>
        <li>A,D</li>
        <li>B</li>


      </ol>
    </div>
    
    
  </section>

</template>

<script>

  export default  {
    name: 'scr-componentes-ingreso',
    props: [],
    mounted () {

    },
     filters : {
      convertir: function(value) {
        var total = value;
          return total.toFixed(2)
        
      }
     },
    
    data () {
      return {
        pesos: 0,
        dolares: 1,

      }
    },
    methods: {
      
    },
    computed: {
      obtenerTotal(){
        //console.log(this.pesos / this.dolares)
        return this.pesos / this.dolares;
      }
      
    }
}


</script>

<style scoped lang="css">
  .scr-componentes-ingreso {
   
  }
   .jumbotron{
     background-color: aquamarine;
    }
</style>
