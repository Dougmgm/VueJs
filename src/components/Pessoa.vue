<template>
    <div>
        <h2>Essa é a descrição da pessoa: {{ nome }}</h2>
        <Info />
    </div>        
</template>

<script>
    import Info from './Info.vue';
    export default {
        name: 'Pessoa',
        components: { // Como esse componente depende de outros componentes é necessario colocar aqui para chamar | Hierarquia está com Info dentro de Pessoa, que está dentro do App
            Info
        },
        data() {
            return {
                nome: 'Douglas'
            }
        }
    }

    /*        <input type="text">
             <input type="text">
        <input type="submit" value="">*/

</script>
