<template>
    <div>
        <button @click="$emit(mudarImagem)">Trocar imagem de perfil</button> <!--Usar o emit para puxar o metodo mudar imagem-->
    </div>
</template>

<script>
    export default {
        name: "MudarImagem",
        emits: ['mudarImagem']
    }
</script>

