<template>
    <div> <!-- Colocar dentro de uma DIV para evitar erros -->
        <h1>Olá Vue!</h1>
        <p>Meu nome é {{ nome }} e minha profissão é {{ profissao }}</p>
    </div>
</template>

<script>
    export default { //Nos componentes pode-se colocar dados, métodos e afins
        name: "PrimeiroComponente",
        data() { //dados dos componentes que retornam em formato de objeto
            return { 
                nome: "Douglas",
                profissao: "Programador"
            }
        }
    }
</script>