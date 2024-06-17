# Four_boxex
[17/06, 21:48] Ritu Navnath Kadam: <!DOCTYPE html>

<html>
<head>
  <meta http-equiv="CONTENT-TYPE" content="text/html; charset=UTF-8">
  <title>Hello, World!</title>
  <link rel="stylesheet" href="ca.css">
  
</head>
<body>
  <div class="box">
  <div class="main">
    <div id="sq1" class="cards"><h1>1</h1></div>
    <div id="sq2"class="cards"><h1>2</h1></div>
  </div>
    <div class="main">
    <div id="sq3"class="cards2"><h1>3</h1></div>
    <div id="sq4"class="cards2"><h1>4</h1></div>
  </div>
  </div>
  <script src="fourboxes.js"></script>
</body>
</html>
[17/06, 21:48] Ritu Navnath Kadam: .main
{
  margin:0;
  padding:0;
  align-items:center;
  justify-content:center;
  display:flex;
}




.cards
{
  width: 100px;
  height: 100px;
  border:2px solid black;
  margin: 5px;
  align-items:center;
  justify-content:center;
  display:flex;
}

   

        
        
.cards2
{
  height:100px;
  width:100px;
  border:2px solid black;
  margin:5px;
  align-items:center;
  justify-content:center;
  display:flex;
  
}
[17/06, 21:49] Ritu Navnath Kadam: let x=document.getElementById("sq1");
x.addEventListener("mouseenter",function(){
    let r= Math.floor(Math.random()*100);
    
     x.innerHTML=`<h1>${r}</h1>`;
})

x.addEventListener("mouseleave",function(){
    x.innerHTML=`<h1>1</h1>`;
})




let y=document.getElementById("sq2");
let clr="red";
y.addEventListener("mouseenter",function(){
    
    if(clr=="red")
    {
        y.style.backgroundColor="red";
        clr="green";
    }
    else if(clr=="green")
    {
        y.style.backgroundColor="green";
        clr="blue";
    }
    else
    {
        y.style.backgroundColor="blue";
        clr="red";
    }
})

y.addEventListener("mouseleave",function(){
    y.style.color="white";
})




let z=document.getElementById("sq3");
z.addEventListener("mouseenter",function(){
    let a=Math.floor(Math.random()*255);
    let b= Math.floor(Math.random()*255);
    let c= Math.floor(Math.random()*255);
    z.style.backgroundColor=`rgb(${a},${b},${c})`;
       
})

z.addEventListener("mouseleave",function(){
    z.style.backgroundColor="white";
    
})


let q=document.getElementById("sq4");

q.addEventListener("mouseenter",function(){
    let a=Math.floor(Math.random()*256);
let b= Math.floor(Math.random()*256);
let c= Math.floor(Math.random()*256);
    let ritu=Math.floor(Math.random()*50);

    x.style.backgroundColor=`rgb(${a},${b},${c})`;
y.style.backgroundColor=`rgb(${c},${a},${b})`;
    z.style.backgroundColor=`rgb(${b},${a},${c})`;
    q.style.color=`rgb(${a},${b},${c})`;
    q.style.fontSize=`${ritu}px`;
   
})             




q.addEventListener("mouseleave",function(){
    x.style.backgroundColor="white";
    y.style.backgroundColor="white";
    z.style.backgroundColor="white";
    
})
