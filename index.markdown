<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "# Your Name\n" +
    "# 8/15/20**\n" +
    "# Create the flock of birds found at https://code.redhawks.us/flock.png\n" +
    "print(&quot;{:&gt;25}&quot;.format(&quot;/^v^\\&quot;))\n" +
    "print(&quot;{:&gt;13}{:&gt;27}&quot;.format(&quot;/^v^\\&quot;,&quot;/^v^\\&quot;))\n" +
    "print(&quot;{:&gt;22}&quot;.format(&quot;/^v^\\&quot;))\n" +
    "print(&quot;{:&gt;8}&quot;.format(&quot;/^v^\\&quot;))";
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
