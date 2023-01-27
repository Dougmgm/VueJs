<template>
  <div>
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
  
  export default {
    name: 'App', //exportando pra JS
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa    
    }
  }
</script>