<!DOCTYPE html>
<html>
<head>
<style>
.div {
  width: 200px;
  height: 100px;
  border: 1px solid black;
}
#hi{
background-color: red;
  width: 2px;
  height: 2px;
  border: 1px solid black;
}
</style>
</head>
<body>

<div class="div" onmousemove="myFunction(event)" ></div>

<div class="div"  >
<div id="hi" ></div>
</div>
<p>Mouse over the rectangle above, and get the coordinates of your mouse pointer.</p>

<p>When the mouse is moved over the div, the p element will display the horizontal and vertical coordinates of your mouse pointer, whose values are returned from the clientX and clientY properties on the 
MouseEvent object.</p>

<p id="demo"></p>

<script>
function myFunction(e) {
  var x = e.clientX;
  var y = e.clientY;
  var coor = "Coordinates: (" + x + "," + y + ")";
 
  move(x,y+100);
  document.getElementById("demo").innerHTML = coor;
}
function move(x,y) {
  var d=document.getElementById("hi");
  d.style.position='absolute';
  d.style.left=x+'px';
  d.style.top=y+'px';
  
}


function clearCoor() {
  document.getElementById("demo").innerHTML = "";
}
</script>

</body>
</html>
