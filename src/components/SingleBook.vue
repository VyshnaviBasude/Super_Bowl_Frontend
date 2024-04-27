<template>
    <div id="maincontainer" :class="book.wonSuperBowlBefore ? 'green': 'red' ">
    <div id="imagecontainer">
    <img v-if="book.conference === 'AFC'" src="../assets/Afc_championship.png" alt="Championship" class="championship-image"/>
    <img v-else src="../assets/Nfc_championship.png" alt="Championship" class="championship-image"/>
</div>
   
    <div id="contentcontainer">
    <p ><strong>Year:</strong> {{ book.year }}</p>
    <p><strong>Winning Team:</strong> {{ book.winningTeam }}</p>
    <p><strong>MVP:</strong> {{ book.superBowlMVP }}</p>
     <p><strong>Conference:</strong> {{ book.conference }}</p>
    <p><strong>Touchdowns:</strong> {{ book.touchdowns }}</p>
    <p><strong>Previous Wins:</strong> {{ book.wonSuperBowlBefore ? 'Yes' : 'No' }}</p>
    <p><strong>Location:</strong> {{ book.location }}</p>
    <p><strong>Average Attendance:</strong> {{ book.averageAttendance }}</p>
    <p><strong>Championships:</strong> {{ book.championships }}</p>
    </div>   
    </div>
</template>

<script>
export default{
    name: 'BookItem',
    props:{
        book: Array
    }
}
</script>

<style scoped>
/*
div{
    background-color: #ffb89e;
    width:60%;
    height:250px;
    align-content: center;
    color: black;
    text-align: center;
    margin-left: 230px;
    border-radius: 10px;

}
*/
#maincontainer
{
 display:flex;
 width:60%;
 margin:0px auto;
 padding:10px;
 text-align: center;
 align-content: center;
 border-radius: 10px;
}

#imagecontainer
{
width:10%;
}

#contentcontainer
{
width:70%;
text-align: center;
margin-left:40px;

}

.championship-image{
width:200px;
margin-top:35px;
margin-left:30px;
}
/* Responsive grid layout */
@media (max-width: 768px) {
.div
  .single-book ,.div{
    width: calc(50% - 30px); 
  }
}

@media (max-width: 480px) {
  .single-book {
    width: calc(100% - 40px); 
  }
}


h1 {
  color: #ffffff; 
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.7); 
}

/* Additional global style adjustments for better appearance */
body {
  margin: 0;
  font-size: 16px;
}

.p {
  margin-bottom: 10px;
  line-height: 2;
 
}

.red{
background-color: white !important;
line-height: 1.5;

}
.green{
    color: black;
    background-color: #BED7DC;
    line-height: 1.5;  
}

</style> 