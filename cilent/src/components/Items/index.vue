<template>
  <div>
    <b-container class="bv-example-row">
    <b-row class="text-left">
         <b-col></b-col>

         <b-col cols="10" class="bg2">
    <h1>รายการชื่อหนังสือการ์ตูน</h1>
  <!--   <p><button v-on:click="logout">Logout</button></p> -->
    <h5>จำนวนชื่อหนังสือการตูน 5 </h5> <hr>

    <div class="box2" >
      <p>หนังสือหมายเลขที่: 1</p>
      <p>ชื่อหน้งสือ: นารูโตะ</p>
      <p>ราคาหนังสือการ์ตูน: 95 บาท</p>
   <div class="img2">
                <p><img src="@/assets/Naruto.jpg"></p>
            </div>
      <hr>

<p>หนังสือหมายเลขที่: 2</p>
      <p>ชื่อหน้งสือ: โดเรม่อน</p>
      <p>ราคาหนังสือการ์ตูน: 85 บาท</p>
   <div class="img2">
                <p><img src="@/assets/Doraemon.jpg"></p>
            </div>
       <hr>

       <p>หนังสือหมายเลขที่: 3</p>
      <p>ชื่อหน้งสือ: วันพีช</p>
      <p>ราคาหนังสือการ์ตูน: 100 บาท</p>
   <div class="img2">
                <p><img src="@/assets/onepiece.jpg"></p>
            </div>
       <hr>

<p>หนังสือหมายเลขที่: 4</p>
      <p>ชื่อหน้งสือ: One-PunchMan</p>
      <p>ราคาหนังสือการ์ตูน: 90 บาท</p>
   <div class="img2">
                <p><img src="@/assets/One_Punch.png"></p>
            </div>
       <hr>

<p>หนังสือหมายเลขที่: 5</p>
      <p>ชื่อหน้งสือ: ดาบพิฆาตอสูร</p>
      <p>ราคาหนังสือการ์ตูน: 100 บาท</p>
   <div class="img2">
                <p><img src="@/assets/as.jpg"></p>
            </div>
       <hr>

    </div>

    

    </b-col>
      <b-col> </b-col>
     </b-row>
</b-container>
  </div>
</template>
<script>

import ItemService from "@/services/ItemsService";
export default {
  data() {
    return {
      items: [],
    };
  },
  async created() {
    this.items = (await ItemService.index()).data;
  }
};
</script>
<style scoped>
div.img2 img {
  width: 150px;
  height: 150px;
}
</style>