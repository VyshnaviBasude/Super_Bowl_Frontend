<template>
<div>
    <h1> {{bookName}} </h1>
    <h4> {{authorName}} </h4>
    <h4> {{yourName}} </h4>
</div>
</template>

<script>
export default{ // Exporting Default Object
    name: 'MyHeader',
    props:{ 

        authorName:String,
        bookName:String,
        yourName: String
    }
}
</script>
<style scoped>

div{
 color:#0C0C0C;
 font-family: "Times New Roman", Times, serif;
 font-size:30px;
    text-align: center;
}
</style>