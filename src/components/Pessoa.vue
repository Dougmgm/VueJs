<template>
    <div>
        <h2>Essa é a descrição da pessoa: {{ nome }}</h2>
        <Info :email="email"/> <!-- email em data é enviado para email de props -->
        <Form />
    </div>        
</template>

<script>
    import Info from './Info.vue';
    import Form from './Form.vue';

    export default {
        name: 'Pessoa',
        components: { // Como esse componente depende de outros componentes é necessario colocar aqui para chamar | Hierarquia está com Info dentro de Pessoa, que está dentro do App
            Info,
            Form
        },
        
        data() {
            return {
                nome: 'Douglas',
                email: "douglas@email.com"
            }
        }
    }

    /*        <input type="text">
             <input type="text">
        <input type="submit" value="">*/

</script>
