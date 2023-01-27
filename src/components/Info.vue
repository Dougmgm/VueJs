<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p> <!-- O "v-if" está puxando a condicional do script, caso o valor da mesma seja "false", logo não irá aparecer na tela -->
        <p v-else>Não estou trabalhando no momento</p> <!-- O else precisa estar logo abaixo do if, do contrário não irá funcionar-->
        <p>Utilizo as seguintes técnologias</p>
        <ul>
            <li>Javascript</li>
            <li>C#</li>
            <li>SQL</li>
        </ul>
        <p v-show="mostrar_email"> Mande um mensagem para {{ email }}</p>
        <p>Para acessar meu portfolio basta clicar <a v-bind:href="meu_link" target="blank">aqui</a></p> <!-- "v-bind" para criar um link de forma dinamica-->
        <Picture />
    </div>    
</template>

<script>
    import Picture from './Picture.vue';

    export default {
    name: "Info",
    components: {
        Picture
    },
    data() {
        return {
            esta_trabalhando: true,
            mostrar_email: true,
            email: "teste@email.com",
            meu_link: "https://www.google.com/"
        };
    }
}
</script>