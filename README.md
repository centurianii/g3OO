g3OO
====

Test some js class libraries with my evaluator: https://github.com/centurianii/g3Evaluator.<br />
My evaluator is an ongoing project.

Testing
=======
Object <code>g3.Evaluator</code> is used to test functioning behaviour.

<h3>How our code is constructed?</h3>
<p>I decided to have the following structure with my files as it helps my server construction in respect with my php framework which is not published at the moment.</p>
<pre>
my source files (g3), necessary libraries (jquery) and my tests folder (tests):
client
  :
  |-jquery
  :  :
  |-g3
  :  |- &lt;g3MyClass.js>
  :  :
  |-view
  |  |-g3evaluator
  |  |  |- g3Evaluator.css
  |  |  |- g3Evaluator.js
  :  :
  |-tests
  |  |-jasmine-standalone-2.0.0
  |  |  |-lib
  |  |  |-spec
  :  :  :
  |  |-g3
  |  :  |- &lt;g3MyClass-SpecRunner.html>
  |  :  |- &lt;g3MyClass-Spec.js>
  |  :  |- &lt;g3MyClass-SpecHelper.js>
  |  :  |- g3Evaluator.html (rename this file to test-g3MyClass.html)
  |  :  |- &lt;test-g3MyClass.html>
  :  :  :
</pre>

There are two <code>g3</code> folders: the one contains the actual code and the other under <code>tests</code> contains the test files.

<h3>In this example I tested 2 libraries:</h3>
<ol>
<li> my.Class which I renamed to g3.Class https://github.com/jiem/my-class and</li>
<li>Class which I renamed to g3.Class https://github.com/DominikGuzei/Class.js</li>
</ol>

One of the benefits of my <code>g3.Evaluator</code> is that there is no name collisions as files are loaded dynamically under user's control.

Test
====
See it there: http://centurianii.github.io/g3OO

Library Errors
==============
<b>https://github.com/DominikGuzei/Class.js</b><br />
<ol>
<li>Found an error on static properties inhereted by grand-childs!!!<br />
Try to run the tab named <i><code>Scientist extends Dreamer</code></i> in panel <i><code>DominikGuzei.Class</code></i> of the <b>evaluator</b>; there you should have <code>scientist1.sleep=undefined, Scientist.sleep=false</code> but instead you have <code>scientist1.sleep=true, Scientist.sleep=false</code>.</li>
</ol>

