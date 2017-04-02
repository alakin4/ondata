---
permalink: /r-starter/
title: "R Starter"
author_profile: true
date: 2017-03-24 01:16:07 +02:00 
tags: r howto notebook
---

{% include rnb-header.html %}

<div class="fluid-row" id="header">

<div class="btn-group pull-right">
<button type="button" class="btn btn-default btn-xs dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false"><span>Code</span> <span class="caret"></span></button>
<ul class="dropdown-menu" style="min-width: 50px;">
<li><a id="rmd-download-source" href="#">Download Rmd</a></li>
</ul>
</div>

</div>

<!-- rnb-text-begin -->
<p>Die ersten Schritte im Umgang mit etwas Neuem sollten immer beginnen mit: Wie mache ich es an, wie mache ich es aus. Bei einer Programmmiersprache wäre das dann: Wie gebe ich etwas ein, wie gebe ich etwas aus. Und zum Ausgeben braucht man ein Ding genannt Variable. Daher fange ich damit an. Wie werden Variablen initialisiert, wie weise ich ihnen einen Wert zu und wie gebe ich sie dann aus. Als erstes die Initalisierung von Variablen und die Wertezuweisung mit <code>=</code>, <code>-&gt;</code> oder <code>&lt;-</code>.</p>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZWluZVZhcmlhYmxlID0gMzJcbmFuZGVyZVZhcmlhYmxlIDwtIDI3XG4xOC43IC0+IGRyaXR0ZVZhcmlhYmxlXG5laW5lVmFyaWFibGVcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">eineVariable =<span class="st"> </span><span class="dv">32</span>
andereVariable &lt;-<span class="st"> </span><span class="dv">27</span>
<span class="fl">18.7</span> -&gt;<span class="st"> </span>dritteVariable
eineVariable</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDMyXG4ifQ== -->
<pre><code>[1] 32</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYW5kZXJlVmFyaWFibGVcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">andereVariable</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDI3XG4ifQ== -->
<pre><code>[1] 27</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZHJpdHRlVmFyaWFibGVcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">dritteVariable</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDE4LjdcbiJ9 -->
<pre><code>[1] 18.7</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZmlyc3RWYXIgPC0gc2Vjb25kVmFyIDwtIFwia29taXNjaFwiXG5hc3NpZ24oXCJ0aGlyZFZhclwiLCAyMilcbmZpcnN0VmFyXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">firstVar &lt;-<span class="st"> </span>secondVar &lt;-<span class="st"> &quot;komisch&quot;</span>
<span class="kw">assign</span>(<span class="st">&quot;thirdVar&quot;</span>, <span class="dv">22</span>)
firstVar</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwia29taXNjaFwiXG4ifQ== -->
<pre><code>[1] &quot;komisch&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuc2Vjb25kVmFyXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">secondVar</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwia29taXNjaFwiXG4ifQ== -->
<pre><code>[1] &quot;komisch&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudGhpcmRWYXJcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">thirdVar</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDIyXG4ifQ== -->
<pre><code>[1] 22</code></pre>
<!-- rnb-output-end -->
<!-- rnb-chunk-end -->
<!-- rnb-text-begin -->
<p>Dann die Ausgabe des Wertes einer Variablen.</p>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuM1xuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="dv">3</span></code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDNcbiJ9 -->
<pre><code>[1] 3</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuMys1XG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="dv">3+5</span></code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDhcbiJ9 -->
<pre><code>[1] 8</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZWluZVZhcmlhYmxlXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">eineVariable</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDMyXG4ifQ== -->
<pre><code>[1] 32</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZWluZVZhcmlhYmxlICsgYW5kZXJlVmFyaWFibGVcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">eineVariable +<span class="st"> </span>andereVariable</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDU5XG4ifQ== -->
<pre><code>[1] 59</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxucHJpbnQoZHJpdHRlVmFyaWFibGUpXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">print</span>(dritteVariable)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDE4LjdcbiJ9 -->
<pre><code>[1] 18.7</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuc2hvdyhkcml0dGVWYXJpYWJsZSArIGVpbmVWYXJpYWJsZSlcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">show</span>(dritteVariable +<span class="st"> </span>eineVariable)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDUwLjdcbiJ9 -->
<pre><code>[1] 50.7</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuY2F0KGZpcnN0VmFyLCBcIixcIiwgc2Vjb25kVmFyLCBcIiAtIHNpbmQgYmVpZGUgZ2xlaWNoIC1cIiwgc2VwID0gXCIgXCIpXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">cat</span>(firstVar, <span class="st">&quot;,&quot;</span>, secondVar, <span class="st">&quot; - sind beide gleich -&quot;</span>, <span class="dt">sep =</span> <span class="st">&quot; &quot;</span>)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoia29taXNjaCAsIGtvbWlzY2ggIC0gc2luZCBiZWlkZSBnbGVpY2ggLVxuIn0= -->
<pre><code>komisch , komisch  - sind beide gleich -</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuY2F0KFwiTmV1ZSBaZWlsZSwgb2Rlcj9cXG5cIilcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">cat</span>(<span class="st">&quot;Neue Zeile, oder?</span><span class="ch">\n</span><span class="st">&quot;</span>)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiTmV1ZSBaZWlsZSwgb2Rlcj9cbiJ9 -->
<pre><code>Neue Zeile, oder?</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYU1lc3NhZ2UgPSBwYXN0ZShmaXJzdFZhciwgXCItXCIsXCJkYXMgaXN0IGRhc3NlbGJlIHdpZVwiLCBzZWNvbmRWYXIsIHNlcCA9IFwiIFwiKVxubWVzc2FnZShhTWVzc2FnZSlcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">aMessage =<span class="st"> </span><span class="kw">paste</span>(firstVar, <span class="st">&quot;-&quot;</span>,<span class="st">&quot;das ist dasselbe wie&quot;</span>, secondVar, <span class="dt">sep =</span> <span class="st">&quot; &quot;</span>)
<span class="kw">message</span>(aMessage)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoia29taXNjaCAtIGRhcyBpc3QgZGFzc2VsYmUgd2llIGtvbWlzY2hcbiJ9 -->
<pre><code>komisch - das ist dasselbe wie komisch</code></pre>
<!-- rnb-output-end -->
<!-- rnb-chunk-end -->
<!-- rnb-text-begin -->
<!-- rnb-text-end -->

<div id="rmd-source-code">LS0tCnRpdGxlOiAiUiBTdGFydGVyIgpvdXRwdXQ6CiAgaHRtbF9ub3RlYm9vazoKICAgIGNvZGVfZm9sZGluZzogbm9uZQogICAgZGZfcHJpbnQ6IGthYmxlCiAgICBoaWdobGlnaHQ6IHB5Z21lbnRzCiAgICB0aGVtZTogZmxhdGx5CiAgaHRtbF9kb2N1bWVudDoKICAgIGhpZ2hsaWdodDogcHlnbWVudHMKLS0tCgpEaWUgZXJzdGVuIFNjaHJpdHRlIGluIGVpbmVyIGV0d2FzIG5ldWVtIGJlZ2lubmVuIGltbWVyIG1pdCBkZW0gdHlwaXNjaGVuOiBXaWUgbWFjaGUgaWNoIGVzIGFuLCB3aWUgbWFjaGUgaWNoIGVzIGF1cy4gQmVpIGVpbmVyIFByb2dyYW1tbWllcnNwcmFjaGUgd8OkcmUgZGFzIGRhbm46IFdpZSBnZWJlIGljaCBldHdhcyBlaW4sIHdpZSBnZWJlIGljaCBldHdhcyBhdXMuIFVuZCB6dW0gQXVzZ2ViZW4gYnJhdWNodCBtYW4gVmFyaWFibGUuIERhaGVyIGZhbmUgaWNoIGRhbWl0IGFuLiBXaWUgd2VyZGVuIFZhcmlhYmxlbiBpbml0aWFsaXNpZXJ0LCB3aWUgd2Vpc2UgaWNoIElobmVuIGVpbmVuIFdlcnQgenUgdW5kIHdpZSBnZWJlIGljaCBldHdhcyBhdXMuCkFscyBlcnN0ZXMgZGllIEluaXRhbGlzaWVydW5nIHZvbiBWYXJpYWJsZW4gdW5kIFdlcnRlenV3ZWlzdW5nIG1pdCA9LCAtPiBvZGVyIDwtLgoKYGBge3J9CmVpbmVWYXJpYWJsZSA9IDMyCmFuZGVyZVZhcmlhYmxlIDwtIDI3CjE4LjcgLT4gZHJpdHRlVmFyaWFibGUKZWluZVZhcmlhYmxlCmFuZGVyZVZhcmlhYmxlCmRyaXR0ZVZhcmlhYmxlCmZpcnN0VmFyIDwtIHNlY29uZFZhciA8LSAia29taXNjaCIKYXNzaWduKCJ0aGlyZFZhciIsIDIyKQpmaXJzdFZhcgpzZWNvbmRWYXIKdGhpcmRWYXIKYGBgCgpEYW5uIGRpZSBBdXNnYWJlIGRlcyBXZXJ0ZXMgZWluZXIgVmFyaWFibGVuLgoKYGBge3J9CjMKMys1CmVpbmVWYXJpYWJsZQplaW5lVmFyaWFibGUgKyBhbmRlcmVWYXJpYWJsZQpwcmludChkcml0dGVWYXJpYWJsZSkKc2hvdyhkcml0dGVWYXJpYWJsZSArIGVpbmVWYXJpYWJsZSkKY2F0KGZpcnN0VmFyLCAiLCIsIHNlY29uZFZhciwgIiAtIHNpbmQgYmVpZGUgZ2xlaWNoIC0iLCBzZXAgPSAiICIpCmNhdCgiTmV1ZSBaZWlsZSwgb2Rlcj9cbiIpCmFNZXNzYWdlID0gcGFzdGUoZmlyc3RWYXIsICItIiwiZGFzIGlzdCBkYXNzZWxiZSB3aWUiLCBzZWNvbmRWYXIsIHNlcCA9ICIgIikKbWVzc2FnZShhTWVzc2FnZSkKYGBgCgoK</div>



</div>

<script>

// add bootstrap table styles to pandoc tables
function bootstrapStylePandocTables() {
  $('tr.header').parent('thead').parent('table').addClass('table table-condensed');
}
$(document).ready(function () {
  bootstrapStylePandocTables();
});

$(document).ready(function () {
  $('.knitsql-table').addClass('kable-table');
  var container = $('.kable-table');
  container.each(function() {

    // move the caption out of the table
    var table = $(this).children('table');
    var caption = table.children('caption').detach();
    caption.insertBefore($(this)).css('display', 'inherit');
  });
});

</script>

<!-- dynamically load mathjax for compatibility with self-contained -->
<script>
  (function () {
    var script = document.createElement("script");
    script.type = "text/javascript";
    script.src  = "https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML";
    document.getElementsByTagName("head")[0].appendChild(script);
  })();
</script>
