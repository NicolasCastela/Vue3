<template>
    <div>
        <h1>Meu formulario</h1>
        <form action=""  @submit="enviarFormulario($event)">
            <div>
                <input type="text" v-model="name">
            </div>  
            <div>
                <input type="text" v-model="email">
            </div>  
                <Submit/>
           

        </form>
    </div>

    <p>Conteudo </p>
    <p>Conteudo </p>
    <p>Conteudo </p>
    <p>Conteudo </p>
    <p>Conteudo </p>
</template>
<script>
import InputText from './Forms/InputText.vue';
import Submit from './Forms/Submit.vue';

export default{
    name:'Form',
    components:{
        InputText,Submit

    },
    data(){
        return{
            name:'',
            email:''


        }
    },
    methods: {
        enviarFormulario(e){
            e.preventDefault();
            
                const name = this.name;
                const email = this.email;
            
            console.log('Formulario enviado')
            console.log('o Nome é: ' + name)
            console.log('o Email é: ' + email)
        }
    }
}
</script>

<style scoped>

p{
 margin-left: 20px;
 height: 35px;
 width: 200px;

}

</style>