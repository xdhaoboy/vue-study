<template>
  <div class="add container">      
      <h1 class="page-header">创建项目</h1>
      <form v-on:submit="addFulllink">
          <div class="well">
            <div>
              <h4>识别服务</h4>
              <div>
                  <label>镜像</label>
                  <input type="text" class="form-control" placeholder="镜像版本" v-model="asr.image">
              </div>
              <div>
                  <label>资源版本</label>
                  <input type="text" class="form-control" placeholder="资源版本" v-model="asr.res">
              </div>
              <div>
                  <label>使用CPU还是GPU</label>
                  <br>
                  <input type="radio" name="computeType" value="cpu"  v-model="asr.computeType" checked>CPU
                  <input type="radio" name="computeType" value="gpu"  v-model="asr.computeType">GPU
              </div>
              <div>
                  <label>资源类型</label>
                  <input type="text" class="form-control" placeholder="aicar" v-model="asr.resType">
              </div>
              <div>
                  <label>音频格式</label>
                  <br>
                  <input type="radio" name="audioType" value="16k" checked v-model="asr.audioType">16k
                  <input type="radio" name="audioType" value="8k"  v-model="asr.audioType">8k
              </div>              
            </div>
            <div>
              <h4>合成服务</h4>
              <div>
                  <label>服务镜像</label>
                  <input type="text" class="form-control" placeholder="image" v-model="tts.image">
              </div>    
              <div>
                  <label>资源地址</label>
                  <input type="text" class="form-control" placeholder="ftp下的路径" v-model="tts.res">
              </div>         
            </div>
            <div>
              <h4>ddsserver</h4>
              <div>
                  <label>服务镜像</label>
                  <input type="text" class="form-control" placeholder="image" v-model="ddsserver.image">
              </div>    
              <div>
                  <label>资源地址</label>
                  <input type="text" class="form-control" placeholder="ftp下的路径" v-model="ddsserver.res">
              </div>         
            </div>
            <div>
              <h4>aidui</h4>
              <div>
                  <label>服务镜像</label>
                  <input type="text" class="form-control" placeholder="image" v-model="aidui.image">
              </div>    
              <div>
                  <label>资源地址</label>
                  <input type="text" class="form-control" placeholder="ftp下的路径" v-model="aidui.res">
              </div>         
            </div>
            <div>
              <h4>dm-dispatch-server</h4>
              <div>
                  <label>服务镜像</label>
                  <input type="text" class="form-control" placeholder="image" v-model="dmdispatch.image">
              </div>    
              <div>
                  <label>资源地址</label>
                  <input type="text" class="form-control" placeholder="ftp下的路径" v-model="dmdispatch.res">
              </div>         
            </div>
            <div>
              <h4>cdmserver</h4>
              <div>
                  <label>服务镜像</label>
                  <input type="text" class="form-control" placeholder="image" v-model="cdmserver.image">
              </div>    
              <div>
                  <label>资源地址</label>
                  <input type="text" class="form-control" placeholder="ftp下的路径" v-model="cdmserver.res">
              </div>         
            </div>
            <div>
              <h4>cnluserver</h4>
              <div>
                  <label>服务镜像</label>
                  <input type="text" class="form-control" placeholder="image" v-model="cnluserver.image">
              </div>    
              <div>
                  <label>资源地址</label>
                  <input type="text" class="form-control" placeholder="ftp下的路径" v-model="cnluserver.res">
              </div>         
            </div>
            <div>
              <h4>cinfoserver</h4>
              <div>
                  <label>服务镜像</label>
                  <input type="text" class="form-control" placeholder="image" v-model="cinfoserver.image">
              </div>    
              <div>
                  <label>资源地址</label>
                  <input type="text" class="form-control" placeholder="ftp下的路径" v-model="cinfoserver.res">
              </div>         
            </div>
            <div>
              <h4>hotword</h4>
              <div>
                  <label>服务镜像</label>
                  <input type="text" class="form-control" placeholder="image" v-model="hotword.image">
              </div>    
              <div>
                  <label>资源地址</label>
                  <input type="text" class="form-control" placeholder="ftp下的路径" v-model="hotword.res">
              </div>         
            </div>
            <div>
              <h4>ezmt</h4>
              <div>
                  <label>服务镜像</label>
                  <input type="text" class="form-control" placeholder="image" v-model="ezmt.image">
              </div>    
              <div>
                  <label>资源地址</label>
                  <input type="text" class="form-control" placeholder="ftp下的路径" v-model="ezmt.res">
              </div>         
            </div>


              <!--div>
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
                  <input type="text" class="form-control" placeholder="profile" v-model="customer.profile"-->
                  <!--textarea class="form-control" rows="10" v-model="customer.profile"></textarea>
              </div-->
              <button type="submit" class="btn btn-primary">添加</button>
          </div>
      </form>

      <form v-on:submit="addASR">
          <div class="well">
            <div class="row">
                <div class="col-lg-12">
                    <div class="input-group">
                    <span class="input-group-addon">
                        <input type="checkbox" aria-label="..."> ASR Lite
                    </span>
                    <span class="input-group-addon">
                        <input type="checkbox" aria-label="..."> TTSLite
                    </span>
                    </div><!-- /input-group -->
                    <div class="input-group">
                    <span class="input-group-addon">
                        <input type="checkbox" aria-label="..."> FullLink
                    </span>
                    <span class="input-group-addon">
                        <input type="checkbox" aria-label="..."> Tranier Server
                    </span>
                    </div><!-- /input-group -->
                </div><!-- /.col-lg-6 -->
            </div>
            <div>
              <h4>识别服务</h4>
              <div>
                  <label>镜像</label>
                  <input type="text" class="form-control" placeholder="镜像版本" v-model="asr.image">
              </div>
              <div>
                  <label>资源版本</label>
                  <input type="text" class="form-control" placeholder="资源版本" v-model="asr.res">
              </div>
              <div>
                  <label>使用CPU还是GPU</label>
                  <br>
                  <input type="radio" name="computeType" value="cpu"  v-model="asr.computeType" checked>CPU
                  <input type="radio" name="computeType" value="gpu"  v-model="asr.computeType">GPU
              </div>
              <div>
                  <label>资源类型</label>
                  <input type="text" class="form-control" placeholder="aicar" v-model="asr.resType">
              </div>
              <div>
                  <label>音频格式</label>
                  <br>
                  <input type="radio" name="audioType" value="16k" checked v-model="asr.audioType">16k
                  <input type="radio" name="audioType" value="8k"  v-model="asr.audioType">8k
              </div>              
            </div>      
              <button type="submit" class="btn btn-primary">添加</button>
          </div>
      </form>
      <form v-on:submit="addTTS">
          <div class="well">
            <div class="row">
                <div class="col-lg-12">
                    <div class="input-group">
                    <span class="input-group-addon">
                        <input type="checkbox" aria-label="..."> ASR Lite
                    </span>
                    <span class="input-group-addon">
                        <input type="checkbox" aria-label="..."> TTSLite
                    </span>
                    </div><!-- /input-group -->
                    <div class="input-group">
                    <span class="input-group-addon">
                        <input type="checkbox" aria-label="..."> FullLink
                    </span>
                    <span class="input-group-addon">
                        <input type="checkbox" aria-label="..."> Tranier Server
                    </span>
                    </div><!-- /input-group -->
                </div><!-- /.col-lg-6 -->
            </div>
            <div>
              <h4>合成服务</h4> 
              <div>
                  <label>服务镜像</label>
                  <input type="text" class="form-control" placeholder="image" v-model="tts.image">
              </div>    
              <div>
                  <label>资源地址</label>
                  <input type="text" class="form-control" placeholder="ftp下的路径" v-model="tts.res">
              </div>   
              <button type="submit" class="btn btn-primary">添加</button>
          </div>
        </div>
      </form>
  </div>
</template>

<script>
export default {
  name: 'add',
  data () {
    return {
        customer:{},
        asr:{},
        tts:{},
        ddsserver:{},
        aidui:{},
        dmdispatch:{},
        cdmserver:{},
        cnluserver:{},
        cinfoserver:{},
        hotword:{},
        ezmt:{}
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
      },
      addASR(e){
          let newAsr = {
              image:this.asr.image,
              res:this.asr.res,
              computeType:this.asr.computeType,
              resType:this.asr.resType,
              audioType:this.asr.audioType
          }

          this.$http.post("http://localhost:3000/users",newAsr)
              .then(function(response){
                  console.log(response)
              })
          
          e.preventDefault();
      },
      addFulllink(e){
          e.preventDefault();},
      addTTS(e){

          let newTts = {
              image:this.tts.image,
              res:this.tts.res
          }

          this.$http.post("http://127.0.0.1:1323/save",newTts)
              .then(function(response){
                  console.log(response)
              })
          e.preventDefault();}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
