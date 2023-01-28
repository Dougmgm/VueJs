<template>
    <div>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Projetos</a></li>
            <li><a href="#">Contatos</a></li>
            <li v-if="esta_logado" ><a href="#">Meu Perfil</a></li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'Header',
        props: ["esta_logado"],
        data() {
            return {

            }
        }
    }
</script>

<style scoped> /*  "Scoped" determina que o estilo só funcionará aqui, não irá vazar para o resto da aplicação */
    ul {
        list-style: none;
        display: flex;
        background-color: #999;
    }
    li {
        margin-right: 10px;
    }

    a {
        color: #ddd;
        text-decoration: none;
        transition: .5s;
    }
    a:hover {
        color: turquoise;
    }
</style>