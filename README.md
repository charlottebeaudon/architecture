<!DOCTYPE html>
<html>
  <style>
  



	body, html {
	max-width: 100%;
	transform: scale(0.8);
	overflow: hidden;
    
	 }
  
  
	.img {
	width:100%;
	}
			
    .mydiv {
	position: absolute;
      z-index: 9;
    }

    .mydivheader {
      padding: 10px;
      cursor: move;
      z-index: 10; 
    
	}
	
	#twentyheight{
	position: absolute;
	top: 2000px;
	left: 2500px;
	}
	
	p{
	font-family: Monospace, Arial;
	font-size: 30px;
	}
		
		.dropdown {
  position: relative;
  display: inline-block;
text-decoration: none !important;
  
}

.dropdown-content {
  display: none;
  position: absolute;

  min-width: 80px;

  z-index: 1;
 
}

.dropdown-content a {
  color: #483D8B;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
  font-size: 19px;

}
a, a:hover,  a:active {
      text-decoration: none;
      color: inherit;
 }

.dropdown-content a:hover {color:#DC143C;}


.dropdown:hover .dropdown-content {display: flex;}

.dropdown:hover .dropbtn {color:black;}


	
  </style>
  <body>
  
  
   <div class="dropdown">
  <button class="dropbtn"> <font size="+2">Works  </font></button>
  
  
  
  
  <div class="dropdown-content">
    <a href="/C:/Users/charlotte/Desktop/architecture/elke/elke.html">Hysteria of Penelope</a>
	<a href="/C:/Users/charlotte/Desktop/architecture/stage/stage.html">La Scala Provence Avignon</a>
    
    <a href="/C:/Users/charlotte/Desktop/architecture/hannes/hannes.html">Oaxaca Sanatorium</a>
	<a href="/C:/Users/charlotte/Desktop/architecture/tschapeller/tschapeller.html">Wreck for Two</a>
    <a href="/C:/Users/charlotte/Desktop/architecture/lacreature/LACRE.html">La+ Creature </a>
	<a href="/C:/Users/charlotte/Desktop/architecture/michelle/michelle.html"> Untitled</a>
	 	
	</div></div>
	
	<div class="dropdown">
	 <button class="dropbtn"><a href="/C:/Users/charlotte/Desktop/architecture/CV.html"> <font size="+2">Curriculum Vitae</font></button></a> 
  <div class="dropdown-content">
    </div></div>
	
    <div class="dropdown">
	 <button class="dropbtn"><font size="+2"><a href="/C:/Users/charlotte/Desktop/architecture/about.html">Contact</font></button></a>
  <div class="dropdown-content">
    </div></div>
</div>
      
	 <br><br><br> <br><br><br>
	
 

<video width="1024" height="576" style="position:absolute top :0px left: 1500px; " loop autoplay muted>
			<source src="elke/videos/Hysteria of Penelope (final)_2.mp4" type="video/mp4">
				Your browser does not support the video tag.
		</video> 

	<div class="mydiv">
      <div class="mydivheader" id="twentyheight"><img src="Screenshot 2022-09-01 185845.jpg" ondblclick="enlargeImg(this)" onclick="resetImg(this)" alt="Screenshot 2022-09-01 185845.jpg" width="27" height="18"></div>
    </div>

	

	

    <script>
	
	 
        //Make the DIV element draggagle:
      var offset = 5;
      var mydivs = document.getElementsByClassName("mydiv");
      for (var i = 0; i < mydivs.length; i++) {
        dragElement(mydivs[i]);
        mydivs[i].style.left = offset + "px";
        offset = offset + mydivs[i].offsetWidth + 5;
      }

      function dragElement(elmnt) {
        var pos1 = 0,
          pos2 = 0,
          pos3 = 0,
          pos4 = 0;
        if (elmnt.getElementsByClassName("mydivheader")[0]) {
          /* if present, the header is where you move the DIV from:*/
          elmnt.getElementsByClassName(
            "mydivheader"
          )[0].onmousedown = dragMouseDown;
        } else {
          /* otherwise, move the DIV from anywhere inside the DIV:*/
          elmnt.onmousedown = dragMouseDown;
        }

        function dragMouseDown(e) {
          e = e || window.event;
          e.preventDefault();
          // get the mouse cursor position at startup:
          pos3 = e.clientX;
          pos4 = e.clientY;
          document.onmouseup = closeDragElement;
          // call a function whenever the cursor moves:
          document.onmousemove = elementDrag;
        }

        function elementDrag(e) {
          e = e || window.event;
          e.preventDefault();
          // calculate the new cursor position:
          pos1 = pos3 - e.clientX;
          pos2 = pos4 - e.clientY;
          pos3 = e.clientX;
          pos4 = e.clientY;
          // set the element's new position:
          elmnt.style.top = elmnt.offsetTop - pos2 + "px";
          elmnt.style.left = elmnt.offsetLeft - pos1 + "px";
        }

        function closeDragElement() {
          /* stop moving when mouse button is released:*/
          document.onmouseup = null;
          document.onmousemove = null;
        }
      }
	  
	 
	 function enlargeImg(img) {
                img.style.transform = "scale(3)";
                img.style.transition =
                  "transform 0.25s ease";
            }
	
	// Function to reset image size
      function resetImg(img) {
        // Set image size to original
        img.style.transform = "scale(1)";
        img.style.transition = "transform 0.25s ease";
      }
	
      
	  
    </script>
	
	
   
  </body>
</html>
