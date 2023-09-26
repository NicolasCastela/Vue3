<template>
    <div>
        <button @click="primeiro(txt1, $event), segundo(txt2,$event), terceiro(txt3, $event)"> Ativar multiplos eventos</button>
        <p>{{ m_p }}</p>
    </div>
</template>



<script>
export default {
    name:'MultiplosEventos',

data() {
    return {
        m_p:'',
        txt1: 'Primeiro Evento',
        txt2: 'Segundo Evento ',
        txt3: ''
    }
},
methods:{
primeiro(txt1, e){
   this.m_p = txt1;
    
},
segundo(txt2, e){
    setTimeout(()=> { this.m_p = txt2;

     },1000)
},
terceiro(txt3,e){
    setTimeout(()=> this.m_p = txt3, 2000)
}

}
}



</script>

<style scoped>
div{
    margin: 50px;
}
</style>