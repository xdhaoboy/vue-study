<template>
  <div class="add container">      
      <h1 class="page-header">添加用户</h1>
      <form v-on:submit="addCustomer">
          <div class="well">
            <div class="row">
                <div class="col-lg-6">
                    <div class="input-group">
                    <span class="input-group-addon">
                        <input type="checkbox" aria-label="..."><p>asr</p>
                    </span>
                    </div><!-- /input-group -->
                </div><!-- /.col-lg-6 -->
            </div>
              <h4>用户信息</h4>
              <div>
                  <label>姓名</label>
                  <input type="text" class="form-control" placeholder="name" v-model="customer.name">
              </div>
              <div>
                  <label>电话</label>
                  <input type="text" class="form-control" placeholder="phone" v-model="customer.phone">
              </div>
              <div>
                  <label>邮箱</label>
                  <input type="text" class="form-control" placeholder="email" v-model="customer.email">
              </div>
              <div>
                  <label>学历</label>
                  <input type="text" class="form-control" placeholder="education" v-model="customer.education">
              </div>
              <div>
                  <label>毕业学校</label>
                  <input type="text" class="form-control" placeholder="graduationschool" v-model="customer.graduationschool">
              </div>
              <div>
                  <label>职业</label>
                  <input type="text" class="form-control" placeholder="profession" v-model="customer.profession">
              </div>
              <div>
                  <label>个人简介</label>
                  <!--input type="text" class="form-control" placeholder="profile" v-model="customer.profile"-->
                  <textarea class="form-control" rows="10" v-model="customer.profile"></textarea>
              </div>
              <button type="submit" class="btn btn-primary">添加</button>
          </div>
      </form>
  </div>
</template>

<script>
export default {
  name: 'add',
  data () {
    return {
        customer:{}
    }
  },
  methods:{
      addCustomer(e){
          //console.log("123");
          if (!this.customer.name || !this.customer.phone ||  !this.customer.email){
              alert("请添加信息");
          } else {
              let newCustomer = {
                  name:this.customer.name,
                  phone:this.customer.phone,
                  email:this.customer.email,
                  education:this.customer.education,
                  graduationschool:this.customer.graduationschool,
                  profession:this.customer.profession,
                  profile:this.customer.profile
              }
              
              this.$http.post("http://localhost:3000/users",newCustomer)
                  .then(function(){
                      //console.log(response)
                      this.$router.push({path:"/",query:{alert:"用户信息添加成功"}})
                  })
          }
          e.preventDefault();
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
