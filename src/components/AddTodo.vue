<template>
  <div>
    <h3>Add Todo</h3>
    <div class="add">
      <form @submit="onSubmit">
        <div class="form-group">
            <input class="form-control col-md-4" type="text" v-model="title" placeholder="Add Todo...">
        </div>
        <input class="btn btn-dark" type="submit" value="Submit">
      </form>
    </div>
  </div>
</template>

<script>
import { mapActions } from 'vuex';
export default {
    name: 'AddTodo',
    data(){
        return{
            title: ''
        };
    },
    methods:{
        ...mapActions(['addTodo']),
        onSubmit(e){
            e.preventDefault();
            this.addTodo(this.title);
        }
    }
}
</script>

<style>

</style>