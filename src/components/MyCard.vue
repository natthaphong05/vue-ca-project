<template lang="">
        <div class="card">
            <div class="image-container">
                <span class="sale">Sale</span>
                <img :src="thumbnail.url" id="Library" style="width:100%">
            </div>
            <div class="container">
                <button class="btn btn-warning">ดูรายละเอียด</button>
                <h5><b>{{name}}</b></h5> 
                <p><span><b>{{specialPrice.amount.value}}</b></span> - <del>{{price.amount.value}}</del></p> 
            </div>
        </div>
</template>

<script>
export default {
    props: ['url_key', 'name', 'thumbnail', 'base_image', 'price', 'specialPrice']
}
</script>

<style scpoed>

.card {
margin: 10px;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  border-radius: 10px;
  font-family: 'Kanit', sans-serif;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.container {
  padding: 2px 16px;
  text-align: center;
}

.btn-warning {
    border-radius: 25px;
    margin-bottom: 10px;
    width: 150px;
}

.btn-warning:hover{
    transform: scale(1.1);
    transition: transform .5s ease;
}

.container span {
    color: red;
}

.image-container{
    position: relative;
    padding: 20px;
}

.sale {
    display: flex;
    position: absolute;
    border-top-right-radius: 7px;
    border-bottom-left-radius: 7px;
	background: red;
	color: white;
	height: 2rem;
	width: 3.5rem;
    justify-content: center;
    align-items: center;
    bottom: 20px;
}

/* #Library:hover {
   content: url("https://img2.pic.in.th/pic/base-1.jpeg");
} */
</style>