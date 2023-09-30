<template>
    <div>
      <img :src="avatar" :alt="descricao">
      <Mudarimg @mudarimg="trocarimg"/>
    </div>
</template>

<script>
import Mudarimg from './Mudarimg.vue';

export default {
    name: 'Picture',
    data() {
        return {
            avatar: '/img/avatar.png',
            descricao: 'Bob sponja'
        };
    },
    components: { Mudarimg },
    methods: {
        trocarimg(){
          this.avatar = "/img/avatar2.png"
          setTimeout(()=> {
            this.avatar="img/avatar.png"}, 2000 )
        }
        
    },
}
</script>