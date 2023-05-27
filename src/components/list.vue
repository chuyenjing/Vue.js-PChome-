<template>
  <div>
    <div class="flex-container_ht">
      <p id="img-back" @click="jump"><img :src="imagePath" /></p>
      <p id="back" @click="jump">🔹回PChome 24h購物首頁</p>
    </div>
    <br><br>
    <div id="input_f">
      <div>
        <span style="font-size: 25px;font-weight: bolder">歡迎登入</span>
        <br><br>
        <span style="font-family:monospace;font-size: 15px;font-weight: 50">
          沒有 PChome 24h購物帳號？
          <b class="reg" @click="register">立即註冊</b>
          <br><br>
          <input type="text" placeholder="請輸入手機號碼或Email" />
          <div class="forget">
            <label class="c-inputLabel">
              <input type="checkbox" class="c-checkbox__input" checked />
              <div class="c-checkbox__checkbox"></div>
              <div class="c-inputLabel__text">記住帳號</div>
            </label>
            <b id="forget_password" @click="forgetPassword">忘記密碼</b>
          </div>
          <br><br>
          <button class="btn success" @click="handleClick">繼續</button>
          <br><br>
          登入帳號，即表示您已閱讀並同意 PChome 之<br><b style="color: #2896EA">會員條款 與 客戶隱私權條款</b>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
import h24 from '@/assets/h24.jpg';
export default {
  data() {
    return {
      imagePath: h24
    };
  },
  methods: {
    handleClick() {
      alert('哈哈');
      this.jump();
    },
    jump() {
      window.location.href = "https://24h.pchome.com.tw/";
    }
  }
}
</script>


<style scoped>
body{
  margin: 0;
  padding: 0;
  background: #F5F5F5;
}

h1, h2, h3, h4, h5, h6 {
  font-weight: normal;
}


.reg{
  cursor: pointer;
  font-weight: 900;
  color: #2591de
}
.reg:hover{
  color: #1e9ccb;
  cursor: pointer;
}
.flex-container_ht {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items:center;
  background-color: white;

}




#input_f {

  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 400px;
  margin: 0 auto;
  width: 400px;
  background-color: white;
}

#back{
  font-size: 14px;
  font-weight: 500;
  cursor: pointer;
  color: #b0abab;
}
#back:hover{
  color: #27acd9;
  cursor: pointer;
}
.forget{
  display: flex;
  justify-content: space-between;
}

.c-inputLabel{
  display: flex;
}
#forget_password{
  color:#2896EA;
  cursor: pointer;

}
#forget_password:hover{
  color: #27acd9;
  cursor: pointer;
}
#img-back{
  cursor: pointer;
}

input[type="text"] {
  height: 35px;
  width: 100%;
  border: 1px solid #d9d9d9;
  border-radius: 10px;
  margin-bottom: 20px;
}


.btn {
  text-align:center ;
  border: none;
  color: white;
  font-size: 16px;
  height: 35px;
  width: 320px;
  border-radius: 10px;
  cursor: pointer;
}

.success {
  background-color: #d10202;
  width: 100%;
}
.success:hover {
  background-color: #ea0126;
}

</style>