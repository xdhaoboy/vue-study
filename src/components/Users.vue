<template>
  <div class="users">
      <h1>hao's 尝试</h1>
      <form v-on:submit="addUser">
          <input type="text" v-model="newUser.name" placeholder="Enter name">
          <input type="text" v-model="newUser.email" placeholder="Enter email">
          <input type="submit" value="submit">
      </form>
      <ul>
          <li v-for="user in users" v-bind:item="user" v-bind:key="user.id">
              {{ user.name }} : {{ user.email }}
          </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'users',
  data () {
    return {
        newUser:{},
        users:[{
            name:"Peter",
            email:"peter@hao.com",
            contacted:false
        },
        {
            name:"Tom",
            email:"tom@hao.com",
            contacted:false
        },
        {
            name:"Jack",
            email:"jack@hao.com",
            contacted:false
        }]
    }
  },
  methods:{
      addUser:function(e){
          console.log("hello")
          e.preventDefault();
          this.users.push({
              name:this.newUser.name,
              email:this.newUser.email,
              contacted:false
          })
          //this.user.
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
  color: purple 
}
</style>
