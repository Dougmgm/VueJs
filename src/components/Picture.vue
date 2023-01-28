<template>
    <img :src="avatar" :alt="descricao"> <!--O "v-bind" está presente mas de forma encurtada, apenas utilizando os dois pontos-->
    <Reutilizacao /> <!--Reutilizado juntamente com o PrimeiroComponente.vue-->
</template>

<script>
    import Reutilizacao from './Reutilizacao.vue';
    export default {
        name: 'Picture',
        components: {
            Reutilizacao
        },
        data() {
            return {
                avatar: "/img/avatar.png",
                descricao: "Douglas Menchon"
            }
        }
    }
</script>