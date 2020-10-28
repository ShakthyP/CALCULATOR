# CALCULATOR
<!DOCTYPE html> 
<html> 
      
<head> 
    <title> 
        EasyCalc 
    </title> 
      
    <!-- CSS property to create interactive 
        calculator interface -->
    <style> 
       body {
              background-image: url("https://c4.wallpaperflare.com/wallpaper/447/848/917/gradient-soft-gradient-minimalism-wallpaper-preview.jpg");
              background-repeat: no-repeat;
              background-color: #cccccc;
			  background-size:cover
              }
			  
         
 
         } 
          
        /* Set the button style */ 
        #btn { 
            width: 100%; 
            height: 40px; 
            font-size: 30px; 
        } 
          
        input[type="button"] {  
            background-color:grey;  
            color: black;  
            border: solid black 2px;  
            width:100%  
        }  
          
        /* Set input textarea */ 
        input[type="text"] {  
            background-color:white;  
            border: solid black 2px;  
            width:98%  
        }  
    </style> 
      
    <script> 
          
        /* Creating function in HTML for backspace operation */ 
        function backspace(calc) {                                              
            size = calc.display.value.length; 
            calc.display.value = calc.display.value.substring(0, size-1); 
        } 
          
        /* Creating function to calculate factorial of element */ 
        function calculate(calc) { 
              
            /* Check if function include ! character then 
            calculate factorial of number */ 
            if(calc.display.value.includes("!")) { 
                  
                size = calc.display.value.length; 
                n = Number(calc.display.value.substring(0, size-1)); 
                f = 1; 
                  
                for(i = 1; i <= n; i++) 
                    f = f*i; 
                calc.display.value = f; 
            } 
              
            /* If function include % character then calculate 
            the % of number */ 
            else if(calc.display.value.includes("%")) { 
                  
                size = calc.display.value.length; 
                n = Number(calc.display.value.substring(0, size-1)); 
                calc.display.value = n%size; 
            } 
  
            else     
                /* Otherwise evalute and execute output */ 
                calc.display.value = eval(calc.display.value); 
        } 
    </script> 
</head> 
  
<body> 
    <h1><center><strong><font color="marron">Welcome!!!</strong></center></h1>
  </br></br>
  <h2><center><strong><font color="marron">Let's start calculating!!!</strong></center></h2>
  </br></br> 
      
    <form name = "calc"> 
          
    <table id = "calc" border="7" align="center" width="550px" height="300px" > 
          
    <tr> 
        <td colspan=6><input id="btn" name="display"
            onkeypress="return event.charCode >= 48 
            && event.charCode <= 57" type="text"> 
        </td> 
    </tr> 
      
    <tr> 
        <td><input id="btn" type="button" value="1"
                OnClick="calc.display.value+='1'"> 
        </td> 
          
        <td><input id="btn" type="button" value="2"
                OnClick="calc.display.value+='2'"> 
        </td> 
          
        <td><input id="btn" type="button" value="3"
                OnClick="calc.display.value+='3'"> 
        </td> 
          
        <td><input id="btn" type="button" value="C"
                OnClick="calc.display.value=''"> 
        </td> 
        <td><input id="btn" type="button" value="<-"
                OnClick="backspace(this.form)"> 
        </td> 
        <td><input id="btn" type="button" value="="
                OnClick="calculate(this.form)"> 
        </td> 
    </tr> 
      
    <tr> 
        <td><input id="btn" type="button" value="4"
                OnClick="calc.display.value+='4'"> 
        </td> 
          
        <td><input id="btn" type="button" value="5"
                OnClick="calc.display.value+='5'"> 
        </td> 
          
        <td><input id="btn" type="button" value="6"
                OnClick="calc.display.value+='6'"> 
        </td> 
          
        <td><input id="btn" type="button" value="-"
                OnClick="calc.display.value+='-'"> 
        </td> 
          
        <td><input id="btn" type="button" value="pi"
                OnClick="calc.display.value+='Math.PI'"> 
        </td> 
          
        <td><input id="btn" type="button" value="cos"
                OnClick="calc.display.value='Math.cos('"> 
        </td> 
    </tr> 
      
    <tr> 
        <td><input id="btn" type="button" value="7"
                OnClick="calc.display.value+='7'"> 
        </td> 
          
        <td><input id="btn" type="button" value="8"
                OnClick="calc.display.value+='8'"> 
        </td> 
          
        <td><input id="btn" type="button" value="9"
                OnClick="calc.display.value+='9'"> 
        </td> 
          
        <td><input id="btn" type="button" value="*"
                OnClick="calc.display.value+='*'"> 
        </td> 
          
        <td><input id="btn" type="button" value="n!"
                OnClick="calc.display.value+='!'"> 
        </td> 
          
        <td><input id="btn" type="button" value="sin"
                OnClick="calc.display.value='Math.sin('"> 
        </td> 
    </tr> 
      
    <tr> 
        <td><input id="btn" type="button" value="."
                OnClick="calc.display.value+='.'"> 
        </td> 
          
        <td><input id="btn" type="button" value="0"
                OnClick="calc.display.value+='0'"> 
        </td> 
          
        <td><input id="btn" type="button" value=","
                OnClick="calc.display.value+=','"> 
        </td> 
          
        <td><input id="btn" type="button" value="+"
                OnClick="calc.display.value+='+'"> 
        </td> 
          
        <td><input id="btn" type="button" value="/"
                OnClick="calc.display.value+='/'"> 
        </td> 
          
        <td><input id="btn" type="button" value="tan"
                OnClick="calc.display.value='Math.tan('"> 
        </td> 
    </tr> 
      
    <tr> 
        <td><input id="btn" type="button" value="log10"
                OnClick="calc.display.value+='Math.log10('"> 
        </td> 
          
		<td><input id="btn" type="button" value="loge"
                OnClick="calc.display.value+='Math.log('"> 
        </td> 
        
          
        <td><input id="btn" type="button" value="^"
                OnClick="calc.display.value+='Math.pow('"> 
        </td> 
          
        <td><input id="btn" type="button" value="("
                OnClick="calc.display.value+='('"> 
        </td> 
          
        <td><input id="btn" type="button" value=")"
                OnClick="calc.display.value+=')'"> 
        </td> 
          
        <td><input id="btn" type="button" value="sqrt"
                OnClick="calc.display.value+='Math.sqrt('"> 
        </td> 
    </tr> 
      
    
    </table> 
    </form> 
</body> 
  
</html>
