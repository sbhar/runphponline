# runphponline
Inspired from 
https://github.com/PHP-Einfach/online-php-editor/blob/master/execute.php

To embed the editor:

```
<!-- Include the dependencies -->
<link rel="stylesheet" id="font-awesome"  href="libs/font-awesome.min.css" type="text/css" />
<script type="text/javascript" src="libs/jquery-2.1.4.min.js"></script>	
<script type="text/javascript" src="libs/ace/ace.js"></script>
<script type="text/javascript" src="libs/FileSaver.js"></script>

<!-- Include the script and css for the online php editor -->	
<link rel="stylesheet" href="css/php-einfach-online-php-editor.css" type="text/css" />
<script type="text/javascript" src="js/php-einfach-online-php-editor.js"></script>


<!-- Include this code snippet where ever you like to have it in your site -->
<div  class="code" id="code_1" data-ace-editor-id="1"
	data-ace-editor-allow-execution="true" data-ace-editor-hide-vars="false" 
	data-ace-editor-script-name="page.php" data-ace-editor-default-get="" data-ace-editor-default-post="">
<pre class="editor" id="code_editor_1" > &lt;?php
echo "Hi and welcome for our Online PHP Editor. The current time is: ".date("H:i:s")." <br />";
echo "Press the button below to execute the code";
?&gt; </pre></div>

<!-- Call this script to transform your HTML code to actual editors -->
<script>
jQuery('div[data-ace-editor-id]').each(function() {
	var url='http://execute.php-einfach.de/execute.php';
	var language = 'en'; //Choose 'de' for German
	new OnlinePHPEditor(this, language, url);
});
</script>
```


