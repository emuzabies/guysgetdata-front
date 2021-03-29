<template>
<div>
<div id="guyscard">
<h5>ต้า Database :</h5>
<a>Form จะใหญ่ไปไหนเนี่ย</a>
<h5>บอมบ์ Full-stack Dev :</h5>
<a>เออว่ะ แต่ขี้เกียจ Deployเว็บใหม่ว่ะ</a>
<h5>ต้า Database :</h5>
<a>แต่เดี๋ยวนะ ตอนที่มึงกำลังใส่โค้ดตอนนี้มันยังไม่Deploy และนี่ขนาดใส่ช่องchatสี ๆ เหมือนหน้าแรกมึงยังไม่ใส่เลย ปล่อยว่างโล้น ๆ</a>
</div>
<div class="card" id="guyscard">
  <div class="card-body">
<form @submit.prevent="handleSubmitForm">
    <h1>กรอกข้อมูลให้ครบถ้วน แล้วกด Submit</h1>
  <div class="form-group">
    <label for="id">StudentID</label>
    <input type="text" class="form-control"  v-model="user.userid" required>
  </div>
  <div class="form-group">
    <label for="FirstName">Firstname</label>
    <input type="text" class="form-control"  v-model="user.firstname" required>
  </div>
  <div class="form-group">
    <label for="LastName">Lastname</label>
    <input type="text" class="form-control"  v-model="user.lastname" required>
  </div>
    <div class="form-group">
    <label for="BirthDate">Birthdate</label>
    <input type="date" class="form-control" v-model="user.birthdate" required>
  </div>
  <div class="form-group">
    <label for="Tel">Tel</label>
    <input type="text" class="form-control"  v-model="user.tel" required>
  </div>
  <div class="form-group">
    <label for="Email">E-mail</label>
    <input type="email" class="form-control"  v-model="user.email" required>
    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
  </div>
  <div class="form-group">
  <button class="btn btn-primary">Submit</button>
  </div>
</form>
  </div>
</div>
</div>
</template>
<script>
import axios from 'axios'
export default {
    data(){
        return{
            user:{
                userid: '',
                firstname: '',
                lastname: '',
                tel: '',
                email: '',
                birthdate: ''
            }
        }
    },
    methods:{
        handleSubmitForm(){
          let apiURL = 'https://guysdata.azurewebsites.net/api/userinfo';

          axios.post(apiURL, this.user).then(() => {
            this.$router.push('/');
            this.$user = {
                userid: '',
                firstname: '',
                lastname: '',
                tel: '',
                email: '',
                birthdate: ''
            }
          }).catch(error => {
            console.log(error)
          })

        }
    }
    
}
</script>
<style scoped>
#guyscard{
  margin: 5px 100px 5px 100px;
}
</style>