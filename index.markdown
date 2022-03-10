<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "#Ask how many hours my great employees worked and calculate their salary and concatenates salary into a tuple\n" +
    "employees = (&quot;Ada Lovelace&quot;,&quot;Grace Hopper&quot;,&quot;Katherine Johnson&quot;,&quot;Margaret Hamilton&quot;,&quot;Megan Smith&quot;)\n" +
    "pay = ()\n" +
    "for employee in employees:\n" +
    "    print(&quot;How many hours did&quot;,employee,&quot;work?&quot;,end = &quot;&quot;)\n" +
    "    hour = float(input())\n" +
    "    salary = hour * 18.75\n" +
    "    pay += (salary,)\n" +
    "    \n" +
    "#blank line in output\n" +
    "print()\n" +
    "for i in range (len(employees)):\n" +
    "    print(&quot;{:20}  {:&gt;7.2f} &quot;.format(employees[i],pay[i]))";
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
