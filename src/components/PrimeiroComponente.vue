<template>
    <div> <!-- Colocar dentro de uma DIV para evitar erros -->
        <h1>Olá Vue!</h1>
        <p>Meu nome é {{ nome }} e minha profissão é {{ profissao }}</p>
        <MultiplosEventos />
        <Reutilizacao /> <!--Reutiliza em diversos lugares ativando um por vez e não todos, ex: carrinho de compras-->
        <Reutilizacao />
        <Reutilizacao />
    </div>
</template>

<script>
    import MultiplosEventos from './MultiplosEventos.vue';
    import Reutilizacao from './Reutilizacao.vue';

    export default { //Nos componentes pode-se colocar dados, métodos e afins
        name: "PrimeiroComponente",
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data() { //dados dos componentes que retornam em formato de objeto
            return { 
                nome: "Douglas",
                profissao: "Programador"
            }
        }
    }
</script>

