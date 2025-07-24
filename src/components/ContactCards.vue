<template>
    <div class="card_section">
     <div class="card_1">
              <i class="bi bi-envelope-fill"></i>
         <h1>Chat to support</h1>
         <p>Speak to our friendly team</p>
     </div>
     <div class="card_2">
         <div class="icon_container">
             <i class="bi bi-envelope-fill"></i>
         </div>
         <h1>Visit Us</h1>
         <p>Visit our office hq</p>
     </div>
     <div class="card_3">
         <div class="icon_container">
             <i class="bi bi-envelope-fill"></i>
         </div>
         <h1>Call Us</h1>
         <p>Mon-fri from 9am to 5pm</p>
     </div>
    </div>
 </template>
 
 <script>
 export default {
 name: 'ContactCards',
 }
 </script>
 
 <style scoped>
   .card_section{
     display: flex;
     justify-content: center;
     row-gap: 1cm;
     column-gap: 1cm;
     padding: 20px 40px;
     background-color:  #151515;
     height: 50vh;
   }
 
   .card_1,
   .card_2,
   .card_3{
     background-color: rgba(6, 5, 5, 0.545);
     padding: 30px;
     height: 40vh;
     width: 40%;
     display: flex;
     flex-direction: column;
     justify-content: center;
     align-items: center;
     border-radius: 10px;
     color: white;
   }
   .card_1 i,
   .card_2 i,
   .card_3 i {
     background: linear-gradient(45deg, #f83201, #ffa600);
     border-radius: 50%;
     width: 64px;
     height: 64px;
     display: flex;
     align-items: center;
     justify-content: center;
     font-size: 2rem;
     margin-bottom: 18px;
     color: white;
   }
   .card_1 h1,
   .card_2 h1,
   .card_3 h1{
     padding-bottom: 5px;
     color: white;
   }
 
   @media screen and (max-width: 1200px){
     *{
         padding: 0;
         margin: 0;
     }
     .card_section{
     display: flex;
     flex-direction: column;
     /* justify-content: center; */
     align-items: center;
     padding: 10px 40px;
     background-color:  #151515;
     height: 150vh;
     }
     
     .card_1,
   .card_2,
   .card_3{
     background-color: rgba(6, 5, 5, 0.545);
     padding: 30px;
     height: 40vh;
     width: 90%;
     display: flex;
     flex-direction: column;
     justify-content: center;
     align-items: center;
     border-radius: 10px;
     color: white;
   }
   }
 
 </style>