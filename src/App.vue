<template>
  <div class="fon">
    <div class="menu">
      <div class="logo"></div>
      <div class="inform"><marquee behavior="scroll" direction="left" >Добро пожаловать на сайт </marquee></div>
    <div class="menuu"><RouterLink to="/">Home</RouterLink> <p style="color:#2c5592">|</p>
    <RouterLink to="/products">Products</RouterLink> <p style="color:#2c5592">|</p> 
    <RouterLink to="/login">Login</RouterLink> <p style="color:#2c5592">|</p> 
    <RouterLink to="/cart">Cart</RouterLink>
    </div></div>
    <RouterView />

  </div>
  <div class="foot">
                        <div class="container-xxl">
                            <div class="row">
<div class="col-12 kapli"><img src="https://demo.themeum.com/html/triangle/1.1/images/home/under.png"></div>


<div class=" col-md-4  col-sm-6 Testimonial"><h2>Testimonial</h2>
     <div class="row">
         <div class="col-md-3"><a href="#"><img src="https://demo.themeum.com/html/triangle/1.1/images/home/profile1.png"></a></div>
    <div class="col-md-9 in-txt"><p>Nisi commodo bresaola, leberkas venison eiusmod bacon occaecat labore tail.</p>
       <h3><a href="#">- Jhon Kalis</a></h3>
    </div></div>

    <div class="row">
    <div class="col-md-3"><a href="#"><img src="https://demo.themeum.com/html/triangle/1.1/images/home/profile2.png"></a>
        
            </div>
            <div class="col-md-9 in-txt"><p>Capicola nisi flank sed minim sunt aliqua rump pancetta leberkas venison eiusmod.</p>
<h3><a href="#">- Abraham Josef</a><n3>
</n3></h3></div>
</div></div>

         <div class="col-md-3  col-sm-6 Contacts">
        <h2>Contacts</h2>
                <p>E-mail:<a href="#"> email@email.com</a></p>
                <p>Phone: +1 (123) 456 7890</p>
            <p>Fax: +1 (123) 456 7891</p>
                <h2>Address</h2>
                <p>Unit C2, St.Vincent's Trading Est.,</p>
                <p>Feeder Road,</p>
            <p>Bristol, BS2 0UY</p>
            <p>United Kingdom</p>
            </div>
        
 <div class=" col-md-4  col-sm-12 Send"> 
<form action="#" method="GET">
    <h2>Send a message</h2>
    <fieldset class="lich">

        <label>
    <input type="text" name="firstname" placeholder="Name" required="">
    </label>
    <label>
    <input type="text" name="surname" placeholder="E-name id" required="">
    </label>
   
    <textarea name="komment" placeholder="Your text here"></textarea>
    <label>
    
    
    
    </label></fieldset>
    <div class="buttons">
    <button type="submit" class="knopka btn-success">Submita</button>

    </div>
    </form></div> 

    <div class="col-sm-12 Company ">
    <p class="white">© Your Company 2014. All Rights Reserved.<br>

Designed by <a href="#" class="a2">Themeum</a></p></div>
                    </div></div>
                </div>
</template>

<script>
import { createClient, provideClient } from '@urql/vue';
export default {
  setup() {
    const client = createClient({
      url: "http://38.242.229.113:8055/graphql",
      fetchOptions: () => {
      
      const token = localStorage.getItem('token')
      return {
        headers: { authorization: token ? `Bearer ${token}` : '' }
      };
    },
    });
    
    provideClient(client);
  }
}
</script>

<style scoped>
.logo{background-image: url("https://cdn.worldvectorlogo.com/logos/apple-4.svg");
width: 55px;
background-size: cover;
 border: 3px solid #53da3f;

}
.fon{background-image: url("https://img.freepik.com/free-photo/blue-sky-with-clouds_1127-282.jpg");
background-size: cover;
width: 100%;
background-attachment:fixed;
}
.inform{ width: 50%;
background-color: #e8e8e6;
background-image:url(https://demo.themeum.com/html/triangle/1.1/images/home/slider-bg.png;),url();background-position-y:bottom;background-repeat:no-repeat;
animation: gorod 5s infinite linear;}    
@keyframes gorod{0%{background-position-x:0%}100%{background-position-x:96% ;}
}
.menu{ 
    
    height: 75px;
    display: flex;
    align-items: center;
    justify-content: space-around;
        border-bottom: 1px solid;
    box-shadow: rgb(44 85 146) 0px 19px 38px -29px inset; 
}
.menu h1{ 
      font-weight: initial;
      font-size: unset;
}
.menuu{ 
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
a{
text-decoration: none;
color: #000000;
padding: 0px 10px 0px 10px;
font-size: unset;
text-transform: uppercase;
font-weight: bold;
}
.pro {
color: black;
     color: #646f81; 
     text-shadow: 7px -4px 3px #646f81, 0 0 0em #657081; 
     text-decoration: line-through; 
    }
    .sto{
     color: #e8e8e6; 
color: black;
     text-shadow: 7px -4px 3px #68748a, 0 0 0em #646f81; 
}
 .header
{background-color: #f6f6f6;} 
.logo{
display: flex;
    justify-content: center;
    font-size: 350%;
    align-items: center;
    margin: 1%;
    height: 10px;
}
.logo{
     display: flex; 
     justify-content: flex-start; 
     font-size: 350%; 
     align-items: center; 
     margin: 1%; 
     padding-left: 1%; 
     color: white;
    background-color: black; 
     height: 62px; 
  text-shadow: 7px -4px 5px #e7dec4, 0 0 5em #e7dec4;
    }

</style>