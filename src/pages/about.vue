<template>
  <div id = "about" class="about">
     <div id="box-border">
        <h1>Improve productivity and be ready for your next exam!</h1>
        <p>This study tracker is designed for you to easily type up all the units, lessons, lecture slides and material that you need to study. </p>
        <p>Simply write down all of those topics and then rate your confidence for each as you continue to prepare for your exam. </p>
        <p>When you're super confident, simply cross out the topic and continue studying on the rest. Once you have completed your study session
          or the exam has passed, click the done button and you are officially free from studying! </p>
        <p> This web page is similar to study sheets that are typically created using paper or some sticky notes. If you aren't used to using something 
          like this, I strongly recommend you try it out and I hope everyone enjoys using it! </p>
          <a :href="'//' + www.github.com/muhanabegum" target="_blank">
  {{ www.github.com/muhanabegum }}
</a>
    </div>
  </div>
</template>

<script> 
export default {
  name: 'About'
}
</script>


<style scoped>
@import url('https://fonts.googleapis.com/css?family=Lato'); 

h1{
  font-family: "Lato"; 
  text-align: center; 
  font-size: 30px; 

}

p{
  text-align: left; 
  padding-top: 20px; 
  font-family: "Lato"; 
  font-size: 20px; 
}

#box-border{
   padding:  35px 90px;
   border-radius: 30px;

}
</style>
