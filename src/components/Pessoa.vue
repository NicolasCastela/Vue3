<template>
    <div>
        <h2> Está a descrição da pessoa : {{ nome }}</h2>
            <Info :email="email"   :esta_trabalhando=true  textoPR='Tenho conhecimentos de: JS, TS, JSX e bla bla bla ' :mostrarPR='mostrarPR' />       
            <Form/>
    </div>
</template>
<script>

import Form from './Form.vue'
import Info from './Info.vue';
export default{
    name: 'Pessoa',
    components: {
        Info,
         Form
    },
    data(){
        return{
            nome:'Nicolas',
            email:'nickcastela@hotmail.com',
            mostrarPR:'PR FEITA EM 29/09'

            
        }}}

</script>