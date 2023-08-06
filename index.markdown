---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# My Parson's problems:

## Make the number 5
<div id="Parson1-sortableTrash" class="sortable-code"></div> 
<div id="Parson1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Parson1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Parson1-newInstanceLink" value="Reset Problem" type="button" /> 
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
    "sortableId": "Parson1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.TurtleGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "executable_code": "",
    "programmingLang": "pseudo",
    "turtleModelCode": "import turtle\nmodelTurtle = turtle.Turtle()\nfor i in range(2):\n    modelTurtle.fd(70)\n    modelTurtle.lt(90)\nfor i in range(2):\n    modelTurtle.fd(70)\n    modelTurtle.rt(90)\nmodelTurtle.fd(70)"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Parson1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Parson1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>








