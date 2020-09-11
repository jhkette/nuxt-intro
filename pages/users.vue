<template>
<div class="container">
    
    <input type="text" v-model="userId">
    <button @click="onLoadUser">Load User</button>
    <!-- render content as nuxt child ie what is on the index page
    and what is on the id page appear where nuxt-child is. THIS FILE HAS TO HAVE THE SAME NAME AS
    THE FOLDER. IE IN THIS CASE USERS -->
    <nuxt-child />
  </div>
    
</template>


<script>
export default {
  data(){
    return {
      userId: ''
    }
  },
  methods: {
    onLoadUser(){
      this.$router.push('/users/' + this.userId)
    }

  },
  layout: 'users'
}
</script>