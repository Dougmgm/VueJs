<template>
    <div>
    <img :src="avatar" :alt="descricao"> <!--O "v-bind" está presente mas de forma encurtada, apenas utilizando os dois pontos-->
    <Reutilizacao /> <!--Reutilizado juntamente com o PrimeiroComponente.vue-->
    <MudarImagem @mudar-imagem="trocarImagem" /> <!--Chamando metodo do emit-->

    </div>
</template>

<script>
    import Reutilizacao from './Reutilizacao.vue';
    import MudarImagem from './MudarImagem.vue';

    export default {
        name: 'Picture',
        components: {
            Reutilizacao,
            MudarImagem
        },
        methods: {
            trocarImagem() {
                this.avatar = "/img/avatar2.png"
            }
        },
        data() {
            return {
                avatar: "/img/avatar.png",
                descricao: "Douglas Menchon"
            }
        }
    }
</script>