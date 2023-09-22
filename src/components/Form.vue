<template>
    <div>
        <form action="">
               <InputText/>
               <InputText/>
                <Submit/>
           

        </form>
    </div>
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

        }
    }
}
</script>

