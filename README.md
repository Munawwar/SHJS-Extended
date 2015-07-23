WARNING: This project is no longer maintained. However, it still works :)

Syntax Highlighter in JavaScript Extended (SHJSX)
===================================================

SHJS (http://shjs.sourceforge.net/) is a source code highlighter written in JavaScript and used for presenting code on the web.

SHJSX is a drop in replacement that extends SHJS with the following new features:
  
1. Added line numbers, based on SHJS-Linenumbers (https://github.com/F1skr/SHJS-Linenumbers/blob/master/src/sh_main.js)
2. A 'Select All' option that copies all the code to the clipboard. This is so you can copy-paste code quickly :)
3. Word highlighting: Click on a word (or select a few letters of the word) in the code, and all occurrences of the word are highlighted.
4. Brace highlighting: Click on a brace and it's matching brace get highlighted. 'Braces' include curly braces {}, square brackets [] and parenthesis ().
5. Code title: Can add a header title to the code snippet (can be used to display something like "mysnippet.js | One line description").


Files
-------

shjsx/ - Is a compressed version ready for deployment. All the js files have been compressed (minified) with YUI compressor (http://developer.yahoo.com/yui/compressor/).

src/ - The uncompressed source code and css.


Usage
-------
Place each source code snippet in a &lt;pre&gt; element. (Currently SHJS cannot highlight code which is not in a pre element.) The pre element must be in the class sh_LANGUAGE, where LANGUAGE specifies the programming language in which the source code is written.

```html
<head>
....
  <link type="text/css" rel="stylesheet" href="css/sh_nedit.css">
  <script type="text/javascript" src="sh_main.js"></script>
  <script type="text/javascript" src="lang/sh_perl.js"></script>
</head>
<body onload="sh_highlightDocument();">

  <pre class="sh-perl">
  #!/usr/bin/perl
  
  use utf8;
  use v5.14;
  use warnings;
  
  say 'Hello World';
  </pre>
</body>
```
Also see example.html.


References
-------------

SHJS documentation is at the original SHJS project (http://shjs.sourceforge.net/).


Thanks to:
SHJS Author and F1skr (https://github.com/F1skr).
