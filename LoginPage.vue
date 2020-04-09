<template>
  <div id="login-page">
    <el-container>
      <el-main>
        <div class="wrap">
          <div class="contain">
            <div class="left-description">
              <el-row>
                <el-col :span="24">
                  <div class="bg-purple">
                    <el-col :span="24">
                      <div class="sidebox">
                        <div class="sidebox__logo">
                          <el-image :src=" loginMesage.url"></el-image>
                        </div>
                        <div class="sidebox__title">
                          <h2>二手家电交易网站</h2>
                        </div>
                      </div>
                      <div class="describe">
                        <h5 style="color:rgb(165, 177, 173)">{{ loginMesage.name}} {{ loginMesage.Ndesc}}</h5>
                        <p>
                          {{ loginMesage.description}}
                        </p>
                      </div>
                      <div class="assion-side-bottom">
                        <el-divider></el-divider>
                        <div class="side-bottom">网站企业版 - 企业级软件协作开发管理平台</div>
                      </div>
                    </el-col>
                  </div>
                </el-col>
              </el-row>
            </div>
            <div class="right-login">
              <el-row>
                <el-col :span="24">
                  <div class="login-page">
                    <el-col :span="24">
                      <div class="session-form__header">
                        <el-col :span="24">
                        <el-menu
                          router
                         :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
                          <el-menu-item index="/login">登录</el-menu-item>
                          <el-menu-item index="/register">注册</el-menu-item>
                        </el-menu>
                     </el-col>
                <el-col :span="24">
              <router-view/>
                 </el-col>
                <el-col :span="24">
                 <el-divider content-position="center">SIGN IN WITH</el-divider>
                 </el-col>
                      
                      </div>
                    </el-col>
                  </div>
                </el-col>
              </el-row>
            </div>
          </div>
        </div>
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "LoginPage",
  data() {
      return {
        loginMesage: {
          url:
            "https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg",
          name: "叶平",
          Ndesc: "本二手家电网站创始人",
          description: `二手家电市场，不仅能带动低消费群体，为人们提供便捷的服务，还能节约资源，使资源重复利用，达到双赢。`
        },
        activeIndex: '1',
      };
    
    
  },
     methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
     }
}
</script>>

<style scoped>
#login-page {
  height: 100%;
}
.el-container {
  height: 100%;
}
.el-main {
  background-color: rgb(243, 240, 240);
  color: #333;
  text-align: center;
}
.wrap {
  width: 800px;
  height: 520px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.contain {
  width: 100%;
  height: 100%;
  border-radius: 3px;
  display: flex;
  box-shadow: 2px 2px 3px 4px rgb(243, 240, 240);
}
.left-description {
  width: 400px;
  height: 100%;
  background-color: #596880;
  border-radius: 2px;
}
.right-login {
  width: calc(100% - 400px);
  height: 100%;
  background-color: white;
  border-radius: 2px;
}
.el-row {
  width: 340px;
  height: 470px;
  transform: translate(8%, 5%);
}
.el-col {
  height: 100%;
  border-radius: 4px;
  text-align: left;
}
.bg-purple {
  height: 100%;
}
.sidebox {
  margin-top: 5px;
  margin-left: 3px;
  height: 90px;
  margin-bottom: 15px;
}
.sidebox__logo {
  width: 220px;
  height: 50px;
}

.sidebox__logo .el-image {
  width: 100px;
  height: 50px;
}
.sidebox__title {
  height: 35px;
}
.sidebox__title > h2 {
  margin-top: 3px;
  line-height: 35px;
  color: #e4e4ea;
}
.describe {
  margin-left: 3px;
  margin-top: 5px;
  height: 200px;
  color: #e4e4ea;
}
.assion-side-bottom {
  margin-top: 80px;
}
.el-divider {
  width: 95%;
  transform: translateX(1%);
}
.side-bottom {
  margin-left: 3px;
  color: #e4e4ea;
}
.login-page {
  width: 100%;
  height: 480px;
}
.session-form__header {
  width: 100%;
  height: 60px;
  padding-left: 4px;
}
.session-form__header .login-header{
font-size: 20px;
}
.el-menu{
  transform: translateX(40%);
  width: 220px;
  height:40px ;
}
.el-menu-item{
  margin-left: 20px;
  padding-bottom: 10px;
}
.el-menu-item:hover{
  color: black;
}
.form_login{
  margin-top: 10px;
  height: 306px;
}
.el-form {
  transform: translateX(-5%);
}

</style>







