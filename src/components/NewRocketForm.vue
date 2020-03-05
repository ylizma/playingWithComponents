<template>
    <div class="mt-5 ">
        <button @click="show=!show" type="button" class="btn btn-danger"> Show Form </button>
    <form v-show="show" @submit.prevent="onAddRocket">
        <div class="form-group">
            <label for="Name">Name</label>
            <input v-model="rocket.name" type="text" class="form-control" id="Name" >
        </div>
        <div class="form-group">
            <label for="Country">Country</label>
            <input v-model="rocket.country" type="text" class="form-control" id="Country" >
        </div>
        <div class="form-group">
            <label for="Image">Image</label>
            <input v-model="rocket.image" type="text" class="form-control" id="Image" >
        </div>
        <div class="form-group">
            <label for="Description">Description</label>
            <textarea v-model="rocket.description" type="text" class="form-control" id="Description" />
        </div>
        <button type="submit" class="btn btn-primary">Add Rocket</button>
    </form>
    </div>
</template>

<script>
function getEmptyRocket(){
    return {
        name:'',
        image:'',
        description:'',
        country:''
    }
}
    export default {
        props:['addRocket'],
        data() {
            return {
                show:false,
                rocket:getEmptyRocket()
            }
        },
        methods:{
            onAddRocket(){
                this.addRocket(this.rocket)
                this.rocket=getEmptyRocket();
                this.show=false;    
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>