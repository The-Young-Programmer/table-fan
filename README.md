
<html>
<title> 
   Project 1
</title>
 <head> 
  <meta name="viewport" content="width=device-width,initial-scale=1"> 
<style type="text/css">
body{
  background:skyblue;
  }
.frame{
  z-index:-2;
  position:relative;
  margin:0 auto;
  width:350px;
  height:350px;
  border-radius:50%;
  border:10px solid white;
  background:radial-gradient(circle at center,white 5%,transparent 5%),
             linear-gradient(transparent 50%,white 50%,white 50.5%,transparent 50.5%),
             linear-gradient(to right,transparent 50%,white 50%,white 50.5%,transparent 50.5%),
             linear-gradient(45deg,transparent 50%,white 50%,white 50.5%,transparent 50.5%),
             linear-gradient(-45deg,transparent 50%,white 50%,white 50.5%,transparent 50.5%);
 transform:scale(0.7);
  }
  .frame::before{
    position:absolute;
    content:"";
    top:100%;
    left:50%;
    width:30px;
    height:100px;
    background:white;
    transform:translate(-50%,0);
    }
 .frame::after{
   position:absolute;
   content:"";
   top:450px;
   left:50%;
   width:100px;
   height:100px;
   background: radial-gradient(circle at 45% 40%,red 4%,transparent 4%),
               radial-gradient(circle at 55% 40%,green 4%,transparent 4%),
     linear-gradient(white 0,white 100%);
   transform:translate(-50%,0);  
   }

  .blade{
    position:absolute;
    background:transparent;
    border:80px solid transparent;
    border-top:120px solid hsl(200,100%,60%);
    border-radius:100px / 200px;
    top:50%;
    left:50%;
    transform:translate(-50%,-60%) rotate(0deg);
    transform-origin:50% 60%;
    }
    
    .blade:nth-child(2){
    transform:translate(-50%,-60%) rotate(120deg);  
     }
      
     .blade:nth-child(3){
       transform:translate(-50%,-60%) rotate(240deg);
      
     }
     
     .wrapper{
       position:absolute;
       top:50%;
       left:50%;
       animation:rot 0.5s infinite linear;
       }
     @keyframes rot{
        to{
          transform: rotate(360deg);
          }
          }
</style>
</head>
 <body> 
<h3> The Young Programmer <br>
Table Fan</h3>
  <div class="frame"> 
   <div class="wrapper"> 
    <div class="blade"></div> 
    <div class="blade"></div> 
    <div class="blade"></div> 
   </div> 
  </div> 
 </body>
</html>
