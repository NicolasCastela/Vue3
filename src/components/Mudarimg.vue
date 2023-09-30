<template>

    <div>
<button @click="$emit('Mudarimg')">Trocar img de perfil </button>
    </div>
</template>

<script>
export default{
name:'Mudarimg',
emits:['Mudarimg']


}
</script>