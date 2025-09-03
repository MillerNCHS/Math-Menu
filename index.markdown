<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "print(&quot;Welcome to the Math Menu Program!&quot;)\n" +
    "num1 = float(input(&quot;Please enter a number: &quot;))\n" +
    "num2 = float(input(&quot;Please enter another number: &quot;))\n" +
    "print(&quot;Math Menu&quot;)\n" +
    "print(&quot;Addition.........Press 1&quot;)\n" +
    "print(&quot;Subtract.........Press 2&quot;)\n" +
    "print(&quot;Multiplication...Press 3&quot;)\n" +
    "print(&quot;Division.........Press 4&quot;)\n" +
    "option = int(input(&quot;What is your menu choice? &quot;))\n" +
    "if (option == 1):\n" +
    "  answer = num1 + num2\n" +
    "elif (option == 2):\n" +
    "  answer = num1 - num2\n" +
    "elif (option == 3):\n" +
    "  answer = num1 * num2\n" +
    "elif (option == 4):\n" +
    "  answer = num1 / num2\n" +
    "else:\n" +
    "  answer = &quot;That was not a menu option.&quot;\n" +
    "print(&quot;The answer is&quot;, answer)";
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
