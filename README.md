

# jQuery Tutorial 

----------------



* Here is the HTML Document

* 1) this is how you inject inside a div or any tag wih the id column

* 

  ```
  <!DOCTYPE html>
  <html>
  	<head>
  		<title>Page Title</title>
  		<script src="https://code.jquery.com/jquery-3.1.1.js"></script>
  	</head>
  	<body>
  		    <div id="start">
  		        
  		    </div>
  		    <div id="second">
  		        
  		        
  		    </div>
  	</body>
  <script>
          $("#start").html("GO");
  </script>
  
  <script>
      var el = document.getElementById("second");
      el.innerHTML = "This is With the Javascript"
      
      
  </script>
  
  </html>
  
  ```

* Writing JavaScript in a separated File all the code have to be written in side this jQuery function

* it is a good practice to load the entire HTML document to be fully loaded and then start the jQuery

* The **$** is used to access jQuery

  

* ```
  $(document).ready(function(){
  	//jQuery code goes here
  
  })
  
  ```

  * But there is a shortcut to do that (this will do the exact same thing as before

    ```
    $(function(){
    	//jQiery code goes here
    });
    ```

    

  ```
  
  ```

  * this code wil change the HTML and override with the jquery

    ```html
    <!-- this is the HTMl code -->
    
    <!DOCTYPE html>
    <html>
      <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
      </head>
      <body>
        <div id="start">Start</div>
      </body>
    </html>
    
    
    ```

    

  * and there goes the jQuery code

    ```
    $(function() {
      $("#start").html("Go!");
    });
    ```

    

* jQuery is used to select the HTMl element and perform "actions" on Them
* Basic Syntax is **  $("#selector").action()  **



```
$("p").hide();
$(".demo").hide()
$("#demo").hide()
```

1) this will hide all the p element

2) this will hide the class named "demo"  <div class="demo">

3) this will hide the element with id name "demo"   <div id="demo">





* To select All the Element like dic we dont use any # or . we directly call them

* ```
  $("div") // selects all the dic class in the document
  
  ```

  

* select the id this code will be use to select

* ```
  $("#test") // select the element with the id="test"
  ```

  

* to select any element based on the class

* ```
  $(".menu") //selects all elements with class="menu"
  ```

  



* example

  ```
  <!DOCTYPE html>
  <html>
    <head>
      <title>Page Title</title>
      <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
      <div id="withid">
          
      </div>
      
      <div class="withclass">
          
      </div>
    </body>
  </html>
  
  
  
  <script>
      
      $("#withid").html("This is the id based extractor");
      $(".withclass").html("this will be extracted with the class");
          
      
  </script>
  ```

* you can select with multiple class and id at the sometime

```
$("div.menu"); // all <div> elements with class menu

$("p:first")    // it wills elect the first p element

$("h1,p")  // select all the h1 and the p element

$("div p") // all <p> elements that are descendants of a <div> element

$("*")  // all elements of the DOM
```



### so suppose you want to select all the links(a element ) inside the paragraph then this code will be used

$("<the parent tag name > <all the clield tag name>")

```
$("p a ");
```



# Example

```
	
```

## if you want to select all the elements that are direct children of div element

suppose you are tried to select element that are inside the div element

```
$("div > *")

```

 

Select the p element and add the data

```
<!DOCTYPE html>
<html>
	<head>
		<title>Page Title</title>
		<script src="https://code.jquery.com/jquery-3.1.1.js"></script>
	</head>
	<body>
		<p id="test">
		    <!-- inject data inside the element -->
		    
		</p>



<script>
    
    $(function() {

    $('#test').html("this is selecting the p element");	
});
</script>

	</body>

</html>


```



* Select all the **p** element  that inside the div "demo"

* this code will hide all the element inside the div emement

  ```
  <!DOCTYPE html>
  <html>
  	<head>
  		<title>Page Title</title>
  		<script src="https://code.jquery.com/jquery-3.1.1.js"></script>
  	</head>
  	<body>
  	    <div class="demo">
  	         <p>
  	             this is inside the demo
  	         </p>
  	         <p>
  	             this is another demo
  	         </p>
  	    </div>
  <script>
      $(function() {
      $("#demo p").hide();
  });
  </script>
  	</body>
  </html>
  
  
  ```





## selecting data and then show the alert message

you can choose the attribute and change it or show it



* here is the HTML

* ```
  <!DOCTYPE html>
  <html>
      <head>
          <title>Page Title</title>
          <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
      </head>
      <body>
          <a href="https://www/facebook.com">Click here</a> 
      </body>
  </html>
  ```

  

* here is the jQuery

* ```
  $(function(){
  	
  	// take the value of the attribute
  	var = $("a").attr("href")
  	// now it have the href attivute value
  	alert(val);
  
  })
  ```

  

### lets change the value so when user clicks the link another link will go we will change the value of the href using the jQuery

this is the html

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
        <a href="https://www.sololearn.com/">Click here</a> 
    </body>
</html>
```



this is jQuery to set the different value

```
// the rule is
$(function(){
	$("<select_tag>").attr("<attr>","set the value");

})
```



```
$(function(){
	$("a")	.attr("href","www.facebook.com")

})
```



## Remove the attribute in the Html document in the hml tag



this html document as two  tags we remove with the jQuery

so after that this will now show op

this is the HTML we remove the boarder and the class

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
       <table border="5" class="tbl" >
           <tr>
               <td>one</td>
               <td>two</td>
           </tr>
           <tr>
               <td>three</td>
               <td>four</td>
           </tr>
       </table>
    </body>
</html>
```

### this is the jQuery

remove the tags this will remove the boarder of the table and the class

```
$("table").removeAttr("border");
$("table").removeAttr("class"); 
```



## Getting the Content of a tag

this is the HTML

```
<p>
  JQuery is <b>fun</b>
  </p>
```



this is the jQuery  data inside the tag

```
$(function(){
	var val = $("p").html()
	alert(val);

})
```



if you only need the content not the tag then text will be used instead of he html

```
$(function(){
	var val = $("p").text()
	alert(val);

})
```

Setting the content

This is the HTML

```
<div id="test">
   <p>some text</p>
</div>

```



```
$(function(){
	var val = $("#text").text("this is the set tetx")
	alert(val);

})
```

#3 getting the value of any HTML tag

The HTML

```
<input type="text" id="name" value="Your Name">
```

```
$(function(){
	alert($("#name").val());
})
```

```
append() //inserts content at the end of the selected elements.
prepend() //inserts content at the beginning of the selected elements.
after() //inserts content after the selected elements.
before() //inserts content before the selected elements
```

## append Text

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
       
       <div class="append">
           <!-- code will be append in here-->
       </div>
    </body>
</html>
```

```
$(function() {
   $(".append").append("appedded text")
});

```

## adding a new total new element in the HTML

```
<p id="demo">Hello</p>
```

```
$(function() {
  var txt = $("<p></p>").text("Hi");
  $("#demo").after(txt);
});
```



### exercise

create a new div element with the text "Hi" and insert it before the element with id="demo".

```
<scrpt>
	// we create a div and inject the hi
	var a = $("<div></div>").text("hi");
	// now inject the new element after the after the ement class "demo"
	$("#demo").after(a);
	
</script>
```





## manipulating the CSS



* you can make a css class and add it to a element using the jQuery	
* here we make a css class and add it with the jquery .not directly

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
        <style>
            .header {
          color: blue;
            font-size:x-large;
}
        </style>
    
     <div>Some text</div>
     
     <script>
         
            $("div").addClass("header");
         
     </script>
    </body>
</html>

```



You can  add multiple class with it and then add it with just space

```
 $("div").addClass("header second third");
```

This is how you remove the CSS class from the div element

```
$("div").removeClass("red");
```



## Toggle class

you can toggle the class . and and change the CSS and from one class to another class

this is the HTML document and we toggle the css of the p class and change its css class

this will also show you how to handle button click event

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
        <style>
            .header {
          color: blue;
            font-size:x-large;
}
        </style>
    
     <div>Some text css will be change and toggled with the button press</div>
     
     <button>
         This is the  button
     </button>
     
     <script>
         
         $(function(){
             $("button").click(function(){
                 
                 $("div").toggleClass("header");
             })
             
         })
     </script>
    </body>
</html>
```



## Just like the html we can also get and set the Css property with Jquery

this code will pop up the current background color and then change the background color into blue 

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
        <style>
            .header {
            background-color:red;    
            color: blue;
            font-size:x-large;
}
        </style>
    
     <div>Some text css will be change and toggled with the button press</div>
     
     <button>
         This is the  button
     </button>
     
     <script>
         
         
         $(function(){
            
            alert($("div").css("background-color")); 
            $("div").css("background-color",'blue');
             
         });
         
     </script>
    </body>
</html>

```



## to set the multiple property of css you need to set it as a json  and pass it

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
        <style>
            .header {
            background-color:red;    
            color: blue;
            font-size:x-large;
}
        </style>
    
     <div>Some text css will be change and toggled with the button press</div>
     
     <button>
         This is the  button
     </button>
     
     <script>
         
         
         $(function(){
            
           $("div").css({"color": "red", "font-size": "200%"});
             
         });
         
     </script>
    </body>
</html>
```

You can add the width and height of a width

```
<script>
         $(function(){            
            $("div").css("background-color", "red");
            $("div").width(100);
            $("div").height(100);
         });
</script>
```

# DOM (MOST IMPORTANT PART Of jQuery)





```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
    <div> div element
        <p>paragraph</p> 
    </div>
    </body>
</html>
```

You can select the parent element and change its attribute and also can change its attribute

```
$(function() {
    
    // changin the element css
    var b = $("p");
    b.css("background-color", "blue");
    
    // changing the parent element 
    var e = $("p").parent();
    e.css("background-color", "red");
});

```



## you can change all the siblings [ all the element inside the same tag]

```
var items = $("div").siblings();
items.hide();

// it will hide all the element inside the all the divs
```





#### removing every child element inside a tag 

you can remove all the siblings inside a div tag using this code

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
        <style>
           div {
             background-color: aqua;
             width: 300px;
             height: 200px;
}
        </style>
    
<div>
   <p style="color:red">Red</p>
   <p style="color:green">Green</p>
   <p style="color:blue">Blue</p>
</div>
     
     <script>
         $("div").empty();
     </script>
  
    </body>
</html>

```

This remove all the value inside the div



# Event using jQuery

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
        <button id="demo">Click Me</button>
        <script>
            $(function(){
                $("#demo").click(function(){
                    $("body").html(Date());
                    
                })
                
            })
            
        </script>
    </body>
</html>
```

This will show the date when the button is clicked



# Another click method is "on" method used for event and the form submitting method



   

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
        <button>Click Me</button>
        
        <script>
            
            $(function(){
                
                $("button").on("click",function(){
                    alert("Cliecked");
                })
            })
            
        </script>
        
    </body>
</html>
```



This will use event to submit the form

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
        
            
    <form action="/action_page.php">
  
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="submit" value="Submit">
    
    </form>
    
    <script>
        
        $(function(){
            
            $("form").on("submit",function(){
                
                alert("hello");
            })
        })
        
    </script>
        
    </body>
</html>
```



Adding the To do list

This is the HTML



```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
       
       <h1>My To-Do List</h1>
        <input type="text" placeholder="New item" />
        <button id="add">Add</button>
        <ol id="mylist"></ol>


    </body>
</html>
```

```
$(function(){
	// make a click event handler
	$("#add").on("click",function(){
		// take the input
		var val = $("input").val();
		if(val !== ""){
			// make a element with the text
			var element = $("<li></li>").text(val);
			// add a button with the element
			$(element).append("<button> Details </button>");
			// now add to the div element
			$("#mylist").append(element);
			// now reset the the input value
			$("input").val("");
		}
	})

})
```





we can animate the button to Increase the button size

this is the html code

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
        <div>Click me</div>
    </body>
</html>
```



```
$(function() {
    $("div").click(function() {
        $("div").animate({
            width: '+=250px',
            height: '+=250px'
        }, 1000);
    });
});
```





## making the dropdown Menu

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
    <div class="menu">
      <div id="item">Dropdown</div>
      <div id="submenu">
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
      </div>
    </div>
    </body>
</html>
```



When the Dropdown menu is clicked this submenu will be shown

```
$(function(){
	$("#item").click(function(){
		$("#submenu").slide(Toggle(500));
	
	});
});
```

