<template>
  <div class="container">


    <h1 class="display-1 fst-italic">Subscribe</h1>
    <div class="body">
      <div>
        <p class="fst-italic">What do you need ?</p>
      </div>
      <div>
        <div class="options">
            <div class="imgOptions">
                <img src="~/assets/img/opt1.jpg" alt="">
            </div>
            <div class="textOptions fw-light">
              <p><strong>Option1:</strong>  Ut tincidunt pellentesque libero, vitae scelerisque leo interdum ac. Morbi volutpat bibendum urna eu condimentum. Sed mollis et felis vel venenatis. Integer ac venenatis turpis. Sed sed tellus sed ex pellentesque pulvinar ac id mauris.</p>
            </div>
            <div class="choiceOptions">
              <p class="label">11.90€/p.m</p>
              <input type="checkbox">
            </div>
        </div>
        <div class="options">
             <div class="imgOptions">
                <img src="~/assets/img/opt2.jpg" alt="">
            </div>
            <div class="textOptions fw-light">
              <p><strong>Option2:</strong>  Ut tincidunt pellentesque libero, vitae scelerisque leo interdum ac. Morbi volutpat bibendum urna eu condimentum. Sed mollis et felis vel venenatis. Integer ac venenatis turpis. Sed sed tellus sed ex pellentesque pulvinar ac id mauris.</p>
            </div>
            <div class="choiceOptions">
              <p class="label">18.90€/p.m</p>
              <input type="checkbox">
            </div>
        </div>
      </div>
    </div>
    <div class="btnSubscribe">
      <button type="button" class="btn btn-outline-dark btn-sm">Subscribe Now !</button>
    </div>

 </div>
</template>

<script>
export default {}
</script>

<style scoped>
.body{
  margin:20px;
}
.options{
  box-shadow: 10px 5px 5px lightgrey;
  margin-top: 20px;
  display:flex;
  align-items:center;
  height: 150px;
  width: 70%;
  border-radius: 10px;
}
input{
  margin: 5px;
}
img{
  width: 150px;
  height: 150px;
  border-radius: 10% 50% 50% 10%;

}
.textOptions{
  margin: 5px;
  font-size: 15px;
}
.choiceOptions{
  display: flex;
  margin: 5px;
  align-items: center
}
.label{
  font-size: 30px;
  margin-right: 5px;
}

.btnSubscribe{
  width: 70%;
  display: flex;
  justify-content: flex-end;
}

</style>
