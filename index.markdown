---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons Practice

## Parsons 1 (Line Based Grader)
Re-arrange the blocks below so they print out a greeting!

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "print(&quot;Hello There!&quot;)\n" +
    "name = input(&quot;What is your name? &quot;)\n" +
    "print(&quot;Good to meet you &quot;, name, &quot;!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
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


## Parsons 2 (Variable Check Grader)
Construct a program that multiplies two values together and prints out the result.

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "num1 = 7\n" +
    "num2 = 3\n" +
    "result = num1 * num2\n" +
    "print(result)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
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

## Parsons 3 (Unit Test Grader)
Your task is to construct a function which returns the index of the largest element in the array.

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "num1 = 7\n" +
    "num2 = 13\n" +
    "if num1 &gt; num2:\n" +
    "	print(&quot;Num1 is bigger than Num2!&quot;)\n" +
    "else:\n" +
    "	print(&quot;Num2 ib bigger than Num1!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
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

## Parsons 4 (Language Translation Grader)
Print out "I am a Java program" three times using a for loop.

<div id="p4-sortableTrash" class="sortable-code"></div>
<div id="p4-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p4-feedbackLink" value="Get Feedback" type="button" />
    <input id="p4-newInstanceLink" value="Reset Problem" type="button" />
</p>
<script type="text/javascript">
(function(){
  var initial = "for (int i=0;i<3;i++) {\n" +
    "System.out.print(\\\"I \\\");\n" +
    "System.out.print(\\\"am \\\");\n" +
    "System.out.print(\\\"a Java program \\\");\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p4-sortable",
    "max_wrong_lines": 1,
    "grader": ParsonsWidget._graders.LanguageTranslationGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "executable_code": "for x in range(3):\n    output += 'I '\n    output += 'am '\n    output += 'a Java program '\npass",
    "programmingLang": "java",
    "vartests": [
        {
            "message": "Testing...",
            "initcode": "output = ''",
            "code": "",
            "variables": {
                "output": "I am a Java program I am a Java program I am a Java program "
            }
        }
    ]
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p4-newInstanceLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.shuffleLines();
  });
  $("#p4-feedbackLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.getFeedback();
   });
})();
</script>


## Parsons 5 (Turtle Grader)
Construct a program by dragging&amp;dropping and reordering lines. The constructed program should draw a triangle like shown below.

<div id="p5-sortableTrash" class="sortable-code"></div>
<div id="p5-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p5-feedbackLink" value="Get Feedback" type="button" />
    <input id="p5-newInstanceLink" value="Reset Problem" type="button" />
</p>
<script type="text/javascript">
(function(){
  var initial = "REPEAT 3 TIMES\n" +
    "  forward(100)\n" +
    "  left(120)\n" +
    "ENDREPEAT";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p5-sortable",
    "max_wrong_lines": 1,
    "grader": ParsonsWidget._graders.TurtleGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "p5-sortableTrash",
    "executable_code": "for i in range(0,3):\nmyTurtle.forward(100)\nmyTurtle.left(120)\npass",
    "programmingLang": "pseudo",
    "turtleModelCode": "modelTurtle.forward(100)\nmodelTurtle.left(120)\nmodelTurtle.forward(100)\nmodelTurtle.left(120)\nmodelTurtle.forward(100)\nmodelTurtle.left(120)",
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p5-newInstanceLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.shuffleLines();
  });
  $("#p5-feedbackLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.getFeedback();
  });
})();
</script>

### Implementation Notes

When you host multiple Parson's problems on a single markdown page, you need to add a unique prefix. You can easily do this in the Codio generator by typing a unique prefix into the "Prefix" textbox and pressing Enter/Return. Then you can simply copy-paste like normal.

If want each problem to be it's own page, you can use relative path links at the bottom of each of your markdown pages as seen below. If you want students to be able to return to previous problems in this format, consider adding previous links or link to a table of contents like page.

### Example Next Link
[Next](./parsons/example1.html)
