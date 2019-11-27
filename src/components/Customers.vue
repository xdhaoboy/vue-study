<template>
  <div class="customers container">
      <Alert v-if="alert" v-bind:message="alert"></Alert>
      <h1 class="page-header">用户管理系统</h1>
      <table class="table talbe-striped">
        <thead>
          <tr>
            <th>姓名</th>
            <th>电话</th>
            <th>邮箱</th>
            <th></th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="customer in customers"  v-bind:item="customer" v-bind:key="customer.id">
            <th>{{customer.name}}</th>
            <th>{{customer.phone}}</th>
            <th>{{customer.email}}</th>
            <th><router-link class="btn btn-default" v-bind:to="'/customer/'+customer.id">详情</router-link></th>
          </tr>
        </tbody>
      </table>
  </div>
</template>

<script>
import Alert from './Alert'
export default {
  name: 'customers',
  data () {
    return {
      customers:[],
      alert:""
    }
  },
  methods:{
    fetchCustomers(){
      this.$http.get("http://localhost:3000/users")
      .then(function(response){
        //console.log(response);
        this.customers = response.body;
      })
    }
  },
  created(){
    if (this.$route.query.alert) {
      this.alert = this.$route.query.alert;
    }
    this.fetchCustomers()
  },
  updated(){
    this.fetchCustomers()
  },
  components:{
    Alert
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
