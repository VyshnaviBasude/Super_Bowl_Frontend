<template>
  <!--Step 3 use the component-->
  <div id="app">
    
  <MyHeader bookName="Super Bowl Winners"/> 
  <BookBox :books=books />
  </div>
 
</template>

<script>
// Step: 1 Import the components
import MyHeader from './components/MyHeader.vue'
import BookBox from './components/BookBox.vue'
export default{
  name: 'App',

  // Step 2: Register the components
  components:{
    MyHeader,
    BookBox
  },
  data(){
    return {
      books: []
    }
  },
  methods:{
    //promoises
    async fetchbooks(){
      const res = await fetch('http://localhost:3666/superBowlWinners');
      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
      this.books = await this.fetchbooks();
  }
}
</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}

div{
  margin-bottom: 0.5em;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
  /* Add your background image below */
  background-image: url('./assets/superbowl.jpg');
  background-size: cover;
  background-position: center center;
  background-attachment: fixed;
  min-height: 100vh;
  width: 100vw;
  overflow-x: hidden;




}

</style>
