<template>
<div>
    <h1>이미지와 라디오버튼 넣어보기</h1>
    <img v-bind:src="imgSrc"/><br/>
    <label><input type="checkbox" value="서울" v-model="checked">서울</label>
    <label><input type="checkbox" value="경기도" v-model="checked">경기도</label>
    <br/>
    <span>체크한 지역{{checked}}</span>
    <br/>
    <div class="container" v-bind:class="{
        'active': isActive, 'text-red': hasError
    }">ClassBinding</div>
</div>
</template>
<style scoped>
 img{
    width: 50%;
 }
 .container{
    width: 100%;
    height: 200px;
 }
 .active{
    background-color: yellow;
    font-weight: bold;
 }
 .text-red{
    color:red;
 }
</style>
<script>
export default {
    data(){
        return{
            name: 'MinDesign',
            imgSrc:"https://cdn.pixabay.com/photo/2013/08/20/15/47/poppies-174276_1280.jpg",
            checked:[],
            isActive: true,
            hasError: false
        }
    }
}
</script>