<template>
  <div class="home">
    <div class="intro text-center">
      <h3>HELLO, I'M OJO</h3>
      <p>
        Passionate about <br />
        <span>UX</span>
        design
      </p>
      <button class=""><span> Read More</span></button>
    </div>

    <div class="projects row m-0 ">
      <div class="cont-1 col-md-6 pb-5 px-0">
        <div class="img-1 d-flex justify-content-center">
          <img
            src="https://res.cloudinary.com/sam-kay/image/upload/v1634483193/ola/1_5_fswzp9.png"
            alt=""
          />
        </div>
      </div>
      <div class="cont-2 col-md-6 pb-5 px-0">
        <div class="img-2 d-flex justify-content-center">
          <img
            src="https://res.cloudinary.com/sam-kay/image/upload/v1634483193/ola/1_5_fswzp9.png"
            alt=""
          />
        </div>
      </div>
      <div class="cont-3 col-md-6 pb-5 px-0">
        <div class="img-3 d-flex justify-content-center">
          <img
            src="https://res.cloudinary.com/sam-kay/image/upload/v1634483193/ola/1_5_fswzp9.png"
            alt=""
          />
        </div>
      </div>
      <div class="cont-4 col-md-6 pb-5 px-0">
        <div class="img-4 d-flex justify-content-center">
          <img
            src="https://res.cloudinary.com/sam-kay/image/upload/v1634483193/ola/1_5_fswzp9.png"
            alt=""
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: "Home",
  components: {},
};
</script>

<style lang="scss" scoped>
.home{
  position:relative;
  top:0;
  z-index:40;
}

.intro {
  padding-top: 120px;

  h3 {
    font-family: Open Sans;
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: 27px;
    letter-spacing: 0em;
  }
  p {
    font-family: Open Sans;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 25px;
    letter-spacing: 0em;
    text-align: center;
    font-size: 18px;
    line-height: 25px;
    color: #abafc1;

    span {
      color: rgba(150, 107, 218, 1);
      font-weight: bolder;
    }
  }

  button {
    padding: 22px 59px;
    border-radius: 15px;
    border: 1px solid #966bda;
    color: #966bda;
    background-color: white;

    &:hover {
      background-color: #966bda;
      color: white;
      transition: 0.4s ease-out;
    }
  }
}

.projects {

  margin-top:72px !important;
 .cont-1{   .img-1 {
    background: rgba(168, 247, 203, 1);
    border-radius: 15px;
  }
 } 

  .cont-2{
   .img-2 {
background: rgba(250, 200, 129, 1);
    border-radius: 15px;
  }
 } 
.cont-3{
   .img-3 {
background: rgba(150, 107, 218, 1);
    border-radius: 15px;

  }
 } 
.cont-4{
   .img-4 {
background: rgba(238, 242, 245, 1);
    border-radius: 15px;

  }
 } 

}

@media (min-width:768px){
   .cont-1{
     padding:0px 20px 20px 0px !important;
     .img-1 {
    
  }
 } 

  .cont-2{
     padding:0px 0px 20px 20px !important;
   .img-2 {
    
  }
 } 
.cont-3{
   padding:20px 20px 0px 0px !important;
   .img-3 {
    
  }
 } 
.cont-4{
   padding:20px 0px 0px 20px !important;
   .img-4 {
    
  }
 } 
}
@media (max-width:768px){
 .projects img{
   width:161px;
   height:161px;
  
 }

 .cont-1, .cont-2, .cont-3, .cont-4 {
   max-width:360px;
   margin:auto;
 }
}
</style>
