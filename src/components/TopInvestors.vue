<template>
  <div class="top_investors">
    <div class="header">
        <h1>Our Top Investors</h1>
    </div>
    <div class="wrapper">
        <div class="investors_card">
        <img src="../assets/Kimberly.jpeg" alt="">
        <h2>Kimberly Leathers</h2>
        <p>invest amount</p>
        <p class="number">1,000,000,000</p>
    </div> 
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.top_investors{
    background-color: #090909e9;
    padding-bottom: 40px;
    padding-top: 40px;
}

.header h1{
    /* width: 55%; */
  font-weight: 800;
  font-size: 49px;
  background: linear-gradient(45deg, #f83201, #ffa600);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
  text-align: center;
}

.investors_card img{
    width: 40vh;
     height: 40vh;
    border-radius: 50%;
    margin-top: 25px;
}

.investors_card{
    /* width: 20%; */
    /* height: 70vh; */
    background-color: #151515;
    border: 2px solid rgba(255, 255, 255, 0.101);
    color: white;
    padding: 0px 15px;
    padding-bottom: 15px;
    border-radius:5px;
}

.investors_card h2{
    text-align: center;
    padding: 10px;
    font-weight: 800;

}

.investors_card p{
    text-align: center;
    padding: 5px;
}

.wrapper{
    display: flex;
    justify-content: center;
    padding-top: 25px;
}

.number{
    color: orangered;
}

@media screen and (max-width: 1200px){
  *{
    padding: 0;
    margin: 0;
  }

  .header h1{
    font-size: clamp(18px, 4vh, 30px);
}
}


</style>