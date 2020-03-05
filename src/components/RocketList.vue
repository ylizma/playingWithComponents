<template>
<div class="row">
    <rocket v-for="(rocket,index) in rockets" 
            :key="index" 
            :rocket="rocket"
            :removeRocket="removeRocket"
            >
    </rocket>
</div>
</template>

<script>
import Rocket from '@/components/Rocket.vue';
    export default {
        props:['rockets','removeRocket'],
        components:{
            Rocket
        }
    }
</script>

<style lang="scss" scoped>

</style>