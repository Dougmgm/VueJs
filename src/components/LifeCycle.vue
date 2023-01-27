<template>
    <h1>Meu nome é: {{ nome }} </h1>
</template>

<script>
    export default {
        name: 'LifeCycle',
        data(){
            return {
                nome: 'Ainda não sei'
            }
        },
        created() {
            setTimeout(()=>{ //delay para executar codigo o que faz o created ser após o mounted
                this.nome = 'Douglas'
            },1000)
            
        },
        mounted(){
            this.nome = 'Juliana' //pela hierarquia o mounted tem prioridade ao created
        }
    }
</script>