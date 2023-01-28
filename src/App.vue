<template>
  <div>
    <Header  :esta_logado="true"/>
    <PrimeiroComponente /> <!-- Após a importação dos dados e a criação do export é possível chamar o .vue diretamente no template-->
    <p>
      O dado de app é: {{ testando }}
      <LifeCycle />
      <Pessoa />
    </p>
  </div>
  
</template>

<script>
  import PrimeiroComponente from './components/PrimeiroComponente.vue'; //importando os dadis da pasta "components"
  import LifeCycle from './components/LifeCycle.vue';
  import Pessoa from './components/Pessoa.vue';
  import Header from './components/Header.vue';
  
  export default {
    name: 'App', //exportando pra JS
    components: {
      Header,
      PrimeiroComponente,
      LifeCycle,
      Pessoa    
    }
  }
</script>

<style>
  body {
    background-color: #333;
    color: #fff;
  }

  a{
    color: red;
  }
</style>