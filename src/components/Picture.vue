<template>
    <img :src="avatar" :alt="descricao"> <!--O "v-bind" está presente mas de forma encurtada, apenas utilizando os dois pontos-->
</template>

<script>
    export default {
        name: 'Picture',
        data() {
            return {
                avatar: "/img/avatar.png",
                descricao: "Douglas Menchon"
            }
        }
    }
</script>