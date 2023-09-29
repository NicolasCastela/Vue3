<template>
    <div>
   
<p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
<p v-else="">Estou em busca de novas Oportunidades</p>
<p>Utilizo as seguintes tecnologias para backend:</p>
<ul>
    <li  v-for="(mostralista, index) in backend_tec" v-bind::key="index">
        {{ mostralista}}</li>

</ul>
<p>ola {{ textoPR }}</p>
<p>ola {{ mostrarPR }}</p>

<ul>
    <li v-for="tec in frontend_tec"  :key="tec.id">
        {{ tec.language }}

    </li>
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
    props:{
        email: String,
        esta_trabalhando: Boolean,
        textoPR: String,
        mostrarPR:String
        },
    data() {
        return {
         
            mostrar_email: false,
           
            meu_link: 'https://google.com',
            textobotao:'Mostrar E-mail',
            backend_tec:['JavaScript', 'PHP', 'Angular'],
            frontend_tec:[
                {id:1, language: 'HTML5'},
                {id:2, language: 'CSS3'},
                {id:3, language: 'VUEE3'}
                ]
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