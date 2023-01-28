<template>
    <div>
        <h2>Meu Formulário</h2>
        <form action="" @submit="enviarFormulario($event)"> <!--"$event" para poder utilizar prevent default-->
            <div>
                <input type="text" v-model="name">
            </div>
            <div>
                <input type="text" v-model="email">
            </div>
            <div>
                <Submit />
            </div>
        </form>
        <p>Conteudos</p>
        <p>Conteudos</p>
        <p>Conteudos</p>
    </div>
</template>

<script>
import InputText from './form/InputText.vue';
import Submit from './form/Submit.vue';

    export default {
    name: 'Form',
    data() {
        return {
            name: '',
            email: ''
        };
    },
    components: { 
        InputText,
        Submit
    },
    methods: {
        enviarFormulario(e) { // O "e" para evitar que o formulario seja enviado
            e.preventDefault();
            const name = this.name
            const email = this.email

            console.log("Formulario enviado")
            console.log("Nome é: " + name)
            console.log("Email é: " + email)
        }
    }
}
</script>

<style scoped>
    p {
        margin: 150px;
    }
</style>