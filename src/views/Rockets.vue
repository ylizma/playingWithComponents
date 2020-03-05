<template>
    <div>
            <newrocketform 
            :addRocket="addRocket">
            </newrocketform>
            
            <listrockets 
            :rockets="rockets"
            :removeRocket="removeRocket"
            >
            </listrockets>
    </div>
</template>

<script>
import newrocketform from '@/components/NewRocketForm.vue';
import listrockets from '@/components/RocketList.vue';
import API from '@/lib/API.js';
    
    export default {
        name:'rockets',
        components:{
            newrocketform,
            listrockets
        },
        data() {
            return {
                rockets:[],
            }
        },
        async mounted() {
            this.rockets=await API.getRockets();
            console.log(this.rockets);  
        },
        methods: {
            addRocket(rocket){
                this.rockets.push(rocket);
            },
            removeRocket(rocket){
                var index=this.rockets.indexOf(rocket)
                this.$delete(this.rockets,index)
            },
        },
    }
</script>

<style lang="scss" scoped>

</style>