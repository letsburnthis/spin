<script>
	
	function rotate(){
	var min = 1000;
  var max = 6000;
  var deg = Math.floor(Math.random() * (max - min)) + min;
  document.getElementById('box').style.transform = "rotate("+deg+"deg)";
	document.getElementById('spin').style.fontSize = "2000%";
		setTimeout(function(){ 			document.getElementById('spin').style.transition = "font-size 0s"; }, 2000);
	setTimeout(function(){ 			document.getElementById('spin').style.fontSize = "1%"; }, 2100);
	
	setTimeout(function(){ 			document.getElementById('spin').style.transition = "font-size 2s"; }, 2200);	
			setTimeout(function(){ 			document.getElementById('spin').style.fontSize = "100%"; }, 2300);
		
}

	
	
	
//<b> bolds text
	
</script>
<body>
	
<div id="mainbox" class="mainbox">

	<div id="box" class="box">
		
		<div class="box1">
      <span class="span1"><b>20 pushups</b></span>
      <span class="span2"><b>30 situps</b></span>
      <span class="span3"><b>40 squats</b></span>
			<span class="span4"><b>10 burpies</b></span>
    </div>
		
  </div>

	<button class="spin" id="spin" on:click={rotate}>WHEEL OF PAIN</button>
	
	<div class="arrow-left"></div>

</div>
	
</body>	


<div>
	
</div>








<style>
	*{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  outline: none;
}

body{
  font-family: "Open Sans";
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  background: rgb(60, 60, 242);

  background-size: cover;
}

	.mainbox{
  position: relative;
  width: 80vw;
  height: 80vw;
}
.mainbox:after{
  position: absolute;
  content: '';
  width: 32px;
  height: 32px;
  background: url('arrow-left.png') no-repeat;
  background-size: 32px;
  right: -30px;
  top: 50%;
  transform: translateY(-50%);
}
.box{
  width: 100%;
  height: 100%;
  position: relative;
  font-weight: bold;
  border-radius: 50%;
  border: 10px solid #fff;
  overflow: hidden;
  transition: all ease 5s;
}

	span{
  width: 50%;
  height: 50%;
  display: inline-block;
  position: absolute;
}
.span1{
  
  background-color: #fffb00;
  top: 0px;
  left: 0;
}
.span2{
  
  background-color: #ff4fa1;
  top: 0px;
  right: 0;
}
.span3{
 
  background-color: #ffaa00;
  bottom: 0;
  left: 0px;
}
	.span4{
 
  background-color: green;
  bottom: 0;
  right: 0px;
}

.box1 .span3 b{
   transform: translate(-50%, -50%) rotate(135deg);
}
.box1 .span1 b{
  transform: translate(-50%, -50%) rotate(215deg);
}
.box1 .span2 b{
  transform: translate(-50%, -50%) rotate(-45deg);
}

.box1 .span4 b{
  transform: translate(-50%, -50%) rotate(45deg);
}

span b{
  font-size: 24px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);

}
	
	
#spin{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 75px;
  height: 75px;
  border-radius: 50%;
  border: 4px solid #fff;
  background-color: BLACK;
  color: #fff;
  box-shadow: 0 5px 20px #000;
  font-weight: bold;
	transition: font-size 2s;
  font-size: 12px;
  cursor: pointer;
}
.spin:active{
	
  width: 70px;
  height: 70px;
  
}


.arrow-left {
	position: absolute;
	top:48%;
	right:0%;
  width: 0; 
  height: 0; 


  border-top: 10px solid transparent;
  border-bottom: 10px solid transparent; 
  
  border-right:10px solid red; 
	
}









</style>
