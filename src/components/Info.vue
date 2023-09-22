<template>
    <div>
      
<p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
<p v-else="">Estou em busca de novas Oportunidades</p>
<p>Utilizo as seguintes tecnologias</p>
<ul>
    <li>JavaScript</li>
    <li>Vue</li>
    <li>React</li>
    <li>Angular</li>
</ul>
<div>
    <button @click="showEmail">{{ textobotao }}  </button>
</div>
<p v-show="mostrar_email">mande uma mensagem para o email: {{ email }}</p>
<p>Para Acessar meu porfólio <a v-bind:href="meu_link" target="_blank">Basta clicar aqui</a></p>
<Picture/>   
</div>
    </template>
    <script >
import Picture from './Picture.vue';

export default{
    name: 'Info',
    data() {
        return {
            esta_trabalhando: false,
            mostrar_email: false,
            email: 'nickcastela@hotmail.com',
            meu_link: 'https://google.com',
            textobotao:'Mostrar E-mail'
        };
    },
    components: { 
        Picture 
    },
         methods: {
       showEmail(){
        this.mostrar_email = !this.mostrar_email
        if(!this.mostrar_email){
            this.textobotao = ' Mostrar E-mail'
        }
            else{
                this.textobotao = 'Esconder E-mail'
            }
        
       }
    }

}

</script>
<style>

p{
    background-color: gainsboro;
}


</style>