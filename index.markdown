---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# My Parson's problems:
## add the new car to the third spot on the list and print the cars.

<div id="parson2-sortableTrash" class="sortable-code"></div> 
<div id="parson2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="parson2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="parson2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "cars = [&#039;McLaren&#039;, &#039;Ferari&#039;, &#039;Bugatti&#039;]\n" +
    "cars.insert($$toggle::0::1::2::3$$, &#039;Rolls-Royce&#039;)\n" +
    "print(cars)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "parson2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.VariableCheckGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "vartests": [
        {
            "message": "print(cars) should return ['McLaren', 'Ferari', 'Rolls-Royce', 'Bugatti']",
            "initcode": "printed = ''",
            "code": "printed = str(cars)",
            "variables": {
                "printed": "['McLaren', 'Ferari', 'Rolls-Royce', 'Bugatti']"
            }
        }
    ]
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#parson2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#parson2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## put your bently in, then take the bugatti out.

<div id="parson3-sortableTrash" class="sortable-code"></div> 
<div id="parson3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="parson3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="parson3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "cars = [&#039;McLaren&#039;, &#039;Ferari&#039;, &#039;Rolls-Royce&#039;, &#039;Bugatti&#039;]\n" +
    "cars.append(&#039;Bentley&#039;)\n" +
    "yourCar = (cars[$$toggle::0::1::2::-5::-4::-3::-2::-1$$])";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "parson3-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.VariableCheckGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "vartests": [
        {
            "message": "Remember, Lists are Indexed from 0, but to start from the end of the list,\nthe last item can be acessed at -1",
            "initcode": "",
            "code": "",
            "variables": {
                "yourCar": "Bugatti"
            }
        }
    ]
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#parson3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#parson3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## park the bugatti between the McLaren and the Ferari, then take out the last car.
<div id="parson4-sortableTrash" class="sortable-code"></div> 
<div id="parson4-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="parson4-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="parson4-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "myCar = &#039;Bugatti&#039;\n" +
    "cars = [&#039;McLaren&#039;, &#039;Ferari&#039;, &#039;Rolls-Royce&#039;, &#039;Bentley&#039;]\n" +
    "cars.insert($$toggle::0::1::2::3::4::-3$$, myCar)\n" +
    "myCar = cars.pop($$toggle::1::2::3:: $$)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "parson4-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.VariableCheckGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "vartests": [
        {
            "message": "Make sure you have parked your car right AND taken the right car. What does an empty pop() do?",
            "initcode": "",
            "code": "parkedCar = str(cars[1])",
            "variables": {
                "myCar": "Bentley",
                "parkedCar": "Bugatti"
            }
        }
    ]
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#parson4-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#parson4-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

# Test problems

## add two numbers 
Change the variables to make the final line print true. Yes, that's a hint to the final line

<div id="parson1-sortableTrash" class="sortable-code"></div> 
<div id="parson1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="parson1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="parson1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "x = $$toggle::5::6::7$$\n" +
    "y = $$toggle::8::9::10$$\n" +
    "z = x + y\n" +
    "print(z == 15) #prints True if z has been set to 15.";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "parson1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.VariableCheckGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "vartests": [
        {
            "message": "print(z == 15) printed \"F alse\"",
            "initcode": "x , y = 0 , 0",
            "code": "",
            "variables": {
                "z": 15
            }
        }
    ]
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#parson1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#parson1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## Make the number 5
Rearrange the code to make the number 5 with a turtle.

<div id="ParsonTurtle-sortableTrash" class="sortable-code"></div> 
<div id="ParsonTurtle-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="ParsonTurtle-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="ParsonTurtle-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "import turtle\n" +
    "modelTurtle = turtle.Turtle()\n" +
    "for i in range(2):\n" +
    "    modelTurtle.fd(70)\n" +
    "    modelTurtle.lt(90)\n" +
    "for i in range(2):\n" +
    "    modelTurtle.fd(70)\n" +
    "    modelTurtle.rt(90)\n" +
    "modelTurtle.fd(70)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "ParsonTurtle-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.TurtleGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "ParsonTurtle-sortableTrash",
    "executable_code": "",
    "programmingLang": "pseudo",
    "turtleModelCode": "import turtle\nmodelTurtle = turtle.Turtle()\nfor i in range(2):\n    modelTurtle.fd(70)\n    modelTurtle.lt(90)\nfor i in range(2):\n    modelTurtle.fd(70)\n    modelTurtle.rt(90)\nmodelTurtle.fd(70)"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#ParsonTurtle-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#ParsonTurtle-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>







