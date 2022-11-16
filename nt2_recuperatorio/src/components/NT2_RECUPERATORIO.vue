<template >

  <section class="src-components-nt-2-recuperatorio">
    <h1>NT2 recuperatorio</h1>
    <label for="">Texto</label>
    <br>
    <input type="text" v-model="texto" />
    <p>{{this.cant(this.texto)}}</p>
    <p>{{this.reemplazarLetras(this.texto)}}</p>
    <p>{{ this.mayus(this.texto) }}</p>
    <p>{{ this.minus(this.texto) }}</p>
    <p>{{ this.intercalado1(this.texto) }}</p>
    <p>{{ this.intercalado2(this.texto) }}</p>
    <p></p>
    <p></p>
    <p></p>
    
    <h1>Respuestas Preguntas EJ 2</h1>
    <p>Pregunta 1: c</p>
    <p>Pregunta 2: b</p>
    <p>Pregunta 3: c</p>
    <p>Pregunta 4: a</p>
    <p>Pregunta 5: b</p>

  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-nt-2-recuperatorio',
    props: [],
    mounted () {

    },
    data () {
      return {
        texto: '',
      }
    },
    methods: {
      cant(text){
        return text.length;
      },
      mayus(text){
        return text.toUpperCase();
      },
      minus(text){
        return text.toLowerCase();
      },
      reemplazarLetras(texto){
        //var split = texto.split('a');
        var t = '';
        
        t = texto.replaceAll('a', 'u');
        t = texto.replaceAll('e', 'o');
        t = texto.replaceAll('o', 'e');
        t = texto.replaceAll('a', 'u');

        return t;

      },
      intercalado1(texto){

        var split = texto.split('');
        
        for(var i in split){
          console.log(i)
          if(i%2===1){
            split[i] = split[i].toUpperCase();
          }
        }

        texto = split.join('');

        return texto;
      },
      intercalado2(texto){

        var split = texto.split('');
        
        for(var i in split){
          console.log(i)
          if(i%2===0){
            split[i] = split[i].toString().toUpperCase();
          }
        }

        texto = split.join('');
        //texto = texto.replaceAll(',');

        return texto;

      },
      /* reemplazarVocalesAxU(text){

      },
      reemplazarVocalesExO(text){

      }, */
    },
    computed: {
      
    }
}


</script>

<style scoped >
  .src-components-nt-2-recuperatorio {

  }
</style>
