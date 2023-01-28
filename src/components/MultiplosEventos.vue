<template>
    <div>
        <button @click="primeiroEvento($event), segundoEvento(e), teceiroEvento(e)">Ativar multiplos eventos</button>
        <p >{{ multiplos_eventos }}</p>
    </div>
</template>

<script>
    export default {
        name: 'MultiplosEventos', 
        data() {
            return {
                multiplos_eventos: "",
            }
        },
        methods: {
            primeiroEvento(e) {
                this.multiplos_eventos = "Primeiro paramêtro ativado" //envia o valor para multiplos eventos de data()
                console.log("teste")
            },
            segundoEvento(e) {
                setTimeout(() => this.multiplos_eventos = "Segundo parâmetro ativado", 1000)
            },
            teceiroEvento(e) {
                setTimeout(()=> this.multiplos_eventos = "Terceiro evento ativado", 2000)
            }
        }
    }
</script>

<style scoped>
    div{
        margin: 100px
    }
</style>