<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p> <!-- O "v-if" está puxando a condicional do script, caso o valor da mesma seja "false", logo não irá aparecer na tela -->
        <p v-else>Não estou trabalhando no momento</p> <!-- O else precisa estar logo abaixo do if, do contrário não irá funcionar-->
        <p>Utilizo as seguintes técnologias</p>
        <ul>
            <li>Javascript</li>
            <li>C#</li>
            <li>SQL</li>
        </ul>
        <p> Mande um mensagem para {{ email }}</p>
    </div>    
</template>

<script>
    export default {
        name: 'Info',
        data() {
            return {
                esta_trabalhando: true, // Booleano, dependedo do valor ele vai intereferir no layout
                mostrar_email: true,
                email: 'teste@email.com'
            }
        }
    }
</script>