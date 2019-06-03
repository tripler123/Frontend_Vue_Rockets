<template>
    <section >
        <button @click="showForm =!showForm" class="btn btn-primary">Show Form</button>
        <form v-if="showForm" @submit.prevent="onAddRocket()">
            <div class="form-group">
                <label for="name">Name</label>
                <input v-model="rocket.name" type="text" name="name" id="Name"  class="form-control" value="" placeholder="Name">
            </div>
            <div class="form-group">
                <label for="country">Country</label>
                <input v-model="rocket.country" type="text" name="country" id="country"  class="form-control" value="" placeholder="country">
            </div>
            <div class="form-group">
                <label for="description">Description</label>
                <textarea v-model="rocket.description" type="text" name="description" id="description"  class="form-control" value="" placeholder="description"></textarea>
            </div>
            <div class="form-group">
                <label for="image">Image</label>
                <input v-model="rocket.image" type="text" name="image" id="image"  class="form-control" value="" placeholder="country">
            </div>
            <button type="submit" class="btn btn-success btn-block">Add Rocket</button>
        </form>
    </section> 
</template>

<script>
function getEmptyRocket(){
    return {
        name: '',
        description:'',
        country:'',
        image:''
    }
};
    export default {
        data() {
            return {
                showForm: false,
                rocket: getEmptyRocket()
            }
        },
        methods:{
            onAddRocket(){
                this.$store.commit('addRocket', this.rocket)
                this.rocket = getEmptyRocket();
                this.showForm = false;
            }
        }
    }
</script>

<style>

</style>