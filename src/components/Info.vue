<template>
    <div>
      
<p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
<p v-else="">Estou em busca de novas Oportunidades</p>
<p>Utilizo as seguintes tecnologias</p>
<p v-show="mostrar_email">mande uma mensagem para o email: {{ email }}</p>
<ul>
    <li>JavaScript</li>
    <li>Vue</li>
    <li>React</li>
    <li>Angular</li>
</ul>
    </div>
    </template>
    <script >
export default{
name:'Info',
data() {
    return {
        esta_trabalhando:false,
        mostrar_email:true,
        email:'nickcastela@hotmail.com'
    }
},

}

</script>