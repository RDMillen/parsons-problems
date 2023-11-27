---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Python Practice Puzzles

## Problem 1 - Hello World Greeting!
Re-arrange the blocks below so they print out a greeting!

<div id="Q1-sortableTrash" class="sortable-code"></div> 
<div id="Q1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Q1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Q1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "name = input(&quot;Hello, what is your name? &quot;)\n" +
    "print(&quot;Nice to meet you &quot;, name, &quot;!&quot;) ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Q1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "Q1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Q1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Q1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## Problem 2 - Quiz Quesiton with an 'if' statement.
Construct a question for a quiz that checks the answer using an if statement.

<div id="Q2-sortableTrash" class="sortable-code"></div> 
<div id="Q2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Q2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Q2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "answer = input(&quot;What do we call a set of instructions for a computer to follow? &quot;)\n" +
    "if answer == &quot;Algorithm&quot; or &quot;algorithm&quot;:\n" +
    "	print(&quot;Correct!&quot;)\n" +
    "else:\n" +
    "	print(&quot;Wrong! Try again next time!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Q2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "Q2-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Q2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Q2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Problem 3 - Input devices.
Create a quesion that allows multiple different answers.

<div id="Q3-sortableTrash" class="sortable-code"></div> 
<div id="Q3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Q3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Q3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "answer = input(&quot;Name an input device: &quot;)\n" +
    "possibleAnswers = [&quot;mouse&quot;, &quot;keyboard&quot;, &quot;microphone&quot;, &quot;webcam&quot;, &quot;controller&quot;]\n" +
    "if answer in possibleAnswers:\n" +
    "	print(&quot;Correct! &quot;, answer, &quot; is an input device!&quot;)\n" +
    "else:\n" +
    "	print(&quot;Incorrect, that is not an input device&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Q3-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "Q3-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Q3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Q3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Problem 4 - Python Turtle
Draw a square using Python Turtle, the "LOOP" block can be adjusted.

<div id="Q4-sortableTrash" class="sortable-code"></div> 
<div id="Q4-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Q4-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Q4-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for i in range(0,$$toggle::2::3::4::$$):\n" +
    "	turtle.fd(50)\n" +
    "	turtle.rt(90)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Q4-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.TurtleGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "Q4-sortableTrash",
    "executable_code": "for i in range(0,$$toggle::2::3::4::$$):\n\tmyTurtle.fd(50)\n\tmyTurtle.rt(90)",
    "programmingLang": "pseudo",
    "turtleModelCode": "for i in range(0,4):\n\tmodelTurtle.fd(50)\n\tmodelTurtle.rt(90)"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Q4-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Q4-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Problem 5 - Countdown While Loop
Create a countdown from 10 to 0, followed by "Blast Off!"

<div id="Q5-sortableTrash" class="sortable-code"></div> 
<div id="Q5-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Q5-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Q5-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "countdown = 10\n" +
    "while countdown &gt; 0:\n" +
    "    print(countdown),\n" +
    "    countdown -= 1\n" +
    "print(&quot;Blastoff!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Q5-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "Q5-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Q5-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Q5-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

