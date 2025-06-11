<template>

    <nav>
      <div class="menu">
       <a class="zy" href="">My Webxite</a>
        <ul>
          <li><a href="">home</a></li>
          <li><a href="">about</a></li>
          <li><a href="">services</a></li>
          <li><a href="">contact</a></li>
        </ul>
      </div>
    </nav>
    <main>
      
     <div class="img"><h1>Welcome To My Website</h1>
      <p>这是我的第一个Vue项目部署演示</p>
      <ul>
        <li v-for="(items,index) in jsb " key="index">{{items}}</li>
        
      </ul>
      <input type="text" v-model="input" @keyup.enter="add">
    </div>
    </main>

</template>

<script setup>
import { reactive, ref } from 'vue';

const jsb=ref([]);
const input=ref(null);
const add=()=>{
  jsb.value.push(input.value);

}


</script>

<style scoped>


*{
  text-decoration: none;
  list-style: none;
  margin: 0;
  padding: 0;
  font-size: 20px;
  overflow-x: hidden; 

}
nav{
  height: 60px;
  width: auto;
  background-color: #333;
  
}
.menu{
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 20px;

}
ul{
  display: flex;
  justify-self: flex-end;
 
}
li{
  margin: 0 10px;
  padding: 0 20px;
  height: 60px;
  line-height: 60px;
  color: aliceblue;
}
a:hover{
  color: rgba(190, 18, 18, 0.8);
  transition: all 0.3s ease-in-out
}
a{
  display: block;
  color: white ;
}
.zy{
  width: auto;
   margin: 10px;
   line-height: 40px;
   font-weight: bold;
}
h1 {
  font-weight: bold;
  font-size: 40px; 
  background: linear-gradient(to right, rgba(255, 14, 14, 0.8), rgba(0, 158, 226, 0.8));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  position: relative;
  overflow: hidden;
}
main .img{
   width: 100vw;
   height: 100vh;
    background-repeat: no-repeat;
   background-position: center;
   background-size: cover;
  background-image: url(https://images.pexels.com/photos/450035/pexels-photo-450035.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260);
}
/* 让内容居中显示 */
.img {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white; 
  
}
</style>