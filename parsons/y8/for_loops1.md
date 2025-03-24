---
layout: default
title: For Loops 1
---

Create a new Turtle Program that will
1. Import the turtle library
2. Initialise the turtle
3. Set the pen colour for the turtle to be blue
4. Draw a triangle

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "import turtle\n" +
    "t = turtle.Turtle()\n" +
    "t.color(&quot;blue&quot;)\n" +
    "for i in range(3):\n" +
    "    t.forward(100)\n" +
    "    t.left(120)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.TurtleGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": false,
    "executable_code": "",
    "programmingLang": "pseudo",
    "turtleModelCode": ""
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
