<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p> <!-- O "v-if" está puxando a condicional do script, caso o valor da mesma seja "false", logo não irá aparecer na tela -->
        <p v-else>Não estou trabalhando no momento</p> <!-- O else precisa estar logo abaixo do if, do contrário não irá funcionar-->
        <p>Utilizo as seguintes tecnologias para backend</p>
        <ul>                            <!--Abaixo item (technology), seguido do array dentro de data (backend_technologies)-->
            <li v-for="(technology, index) in backend_technologies" v-bind:key="index"> <!--Key serve para evitar loops -->
                {{technology}}
            </li> <!--Colocar no li para repetir dados da lista e não a lista em si (ul)-->
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end</p>
        <ul>
            <li v-for="technology in frontend_technologies" :key="technology.id"> <!--Puxando dados de um objeto-->
                {{ technology.language }} <!--Puxa language contido em technology-->
            </li>
        </ul>
        <div>
            <button @click="showEmail">{{texto_botao}}</button> <!-- Primeiro está o método de mostrar email, em seguida puxando os dados da "data()" -->
        </div>
        <p v-show="mostrar_email"> Mande um mensagem para {{ email }}</p>
        <p>Para acessar meu portfolio basta clicar <a v-bind:href="meu_link" target="blank">aqui</a></p> <!-- "v-bind" para criar um link de forma dinamica-->
        <Picture />
        <!-- <Form /> -->
    </div>    
</template>

<script>
    import Picture from './Picture.vue';
    // import Form from './Form.vue'

    export default {
    name: "Info",
    components: {
        Picture,
        // Form
    },
    data() {
        return {
            esta_trabalhando: true,
            mostrar_email: false,
            email: "teste@email.com",
            meu_link: "https://www.google.com/",
            texto_botao: "Mostar Email",
            backend_technologies: ["Javascript", "PHP", "Python"], //formato array
            frontend_technologies: [ //formato objeto
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'Vue'}
            ]
        }
    },
    methods: {
        showEmail(){
            this.mostrar_email = !this.mostrar_email //o "!" significa ao contrário
            if (!this.mostrar_email) {
                this.texto_botao = 'Mostrar e-mail'
            } else {
                this.texto_botao = 'Ocultar botão'
            }
        }
    }
}
</script>