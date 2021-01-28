<template>
  <div class="container">
    <h1 class="display-1 fst-italic">Welcome to <span style="color:green;">"Just one <strong>G</strong>"</span></h1>

    <div class="body">
      <div>
        <video autoplay loop >
            <source src="~/assets/video/vid1.webm" type="video/webm">
            <source src="~/assets/video/vid1.mp4" type="video/mp4">
            Sorry, your browser doesn't support embedded videos.
        </video>
      </div>
      <div>
         <p class="fst-italic">"On this app you can order only 1 <span style="color:green;"><strong>G</strong></span>ram of each strain, <br>
       Or subscribe to our monthly subscription and receive  <span style="color:green;"><strong>JoG</strong></span>/month <br>
       of best weed quality, enjoy..."</p>
      </div>
    </div>

  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.container{
  display:flex;
  flex-direction:column;
  align-items:flex-start;
}
p{
  margin-top: 50px;
  text-align: right;
}
.body{
  display: flex;
  margin-top: 40px;

}
video{
height: 300px;
}


</style>
