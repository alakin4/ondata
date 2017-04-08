---
permalink: /r-starter/
title: "R Starter"
author_profile: true
rnotebook: true
date:  2017-04-06 01:12:46 +02:00 
last_modified_at: 2017-04-08 01:12:56 +02:00 
tags: r howto notebook
---

{% include rnb__header.html %}

<!-- source download -->
<script>
$(document).ready(function () {
  window.initializeSourceDownload("{{site.baseurl}}/assets/download/rnb-r-starter.Rmd","rnb-r-starter.Rmd");
});
</script>

<div class="fluid-row" id="header">

<div class="btn-group pull-right">
<button type="button" class="btn btn-default btn-xs dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false"><span>Code</span> <span class="caret"></span></button>
<ul class="dropdown-menu" style="min-width: 50px;">
<li><a id="rmd-download-source" href="#">Download Rmd</a></li>
</ul>
</div>

</div>

<!-- rnb-text-begin -->
<div id="r-lernen" class="section level2">
<h2>R lernen</h2>
<p>Ich bin bei XDA auf einige Online Kurse über Machine Learning gestoßen. Und da ich darüber schon immer mehr wissen wollte und neuer Kopf-Input gerade anstand, habe ich angefangen den Kurs zu schauen. Ich erinnerte mich außerdem, während des US Wahlkampfs diesen spannenden Artikel <a href="http://varianceexplained.org/r/trump-tweets/" target="_blank">Text analysis of Trump’s tweets confirms he writes only the (angrier) Android half</a> gelesen zu haben. Das wollte ich auch können. Also war es an der Zeit, das ganz alte Statistik-Wissen zu reanimieren und einzusteigen. Der Artikel ist nur eine Sammlung der ersten Tutorials über die Grundlagen von R – Variablen, Ein- und Ausgabe, Operationen. Eigenlich für mich als Wiederholung geschrieben. Vielleicht kriegt ja noch jemand lust, R auszuprobieren. Alles wir heute mit Torten und Balken begründet und wir +glauben+, sobald wir eine begründete Grafik sehen. Ich denke, man sollte sie auch selbst herstellen können.</p>
</div>
<div id="variablen-zuweisung-und-ausgabe" class="section level2">
<h2>Variablen: Zuweisung und Ausgabe</h2>
<p>Die ersten Schritte im Umgang mit etwas Neuem sollten immer beginnen mit: Wie mache ich es an, wie mache ich es aus. Bei einer Programmmiersprache wäre das dann: Wie gebe ich etwas ein, wie gebe ich etwas aus. Und zum Ausgeben braucht man ein Ding genannt Variable. Daher fange ich damit an. Wie werden Variablen initialisiert, wie weise ich ihnen einen Wert zu und wie gebe ich sie dann aus. Als erstes die Initalisierung von Variablen und die Wertezuweisung mit =, -&gt; oder &lt;-. Und natürlich deren Ausgabe.</p>
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
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZmlyc3RWYXIgPC0gc2Vjb25kVmFyIDwtIFwia29taXNjaFwiXG5jYXQoZmlyc3RWYXIsIFwiLFwiLCBzZWNvbmRWYXIsIFwiIC0gc2luZCBiZWlkZSBnbGVpY2ggLVwiLCBzZXAgPSBcIiBcIilcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">firstVar &lt;-<span class="st"> </span>secondVar &lt;-<span class="st"> &quot;komisch&quot;</span>
<span class="kw">cat</span>(firstVar, <span class="st">&quot;,&quot;</span>, secondVar, <span class="st">&quot; - sind beide gleich -&quot;</span>, <span class="dt">sep =</span> <span class="st">&quot; &quot;</span>)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoia29taXNjaCAsIGtvbWlzY2ggIC0gc2luZCBiZWlkZSBnbGVpY2ggLVxuIn0= -->
<pre><code>komisch , komisch  - sind beide gleich -</code></pre>
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
</div>
<div id="datentypen" class="section level2">
<h2>Datentypen</h2>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaWNoQmluSW50ZWdlciA8LSA0TFxuaXMuaW50ZWdlcihpY2hCaW5JbnRlZ2VyKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">ichBinInteger &lt;-<span class="st"> </span>4L
<span class="kw">is.integer</span>(ichBinInteger)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFRSVUVcbiJ9 -->
<pre><code>[1] TRUE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaWNoQmluQXVjaEludGVnZXIgPC0gYXMuaW50ZWdlcigzKzUpXG5jbGFzcyhpY2hCaW5BdWNoSW50ZWdlcilcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">ichBinAuchInteger &lt;-<span class="st"> </span><span class="kw">as.integer</span>(<span class="dv">3+5</span>)
<span class="kw">class</span>(ichBinAuchInteger)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiaW50ZWdlclwiXG4ifQ== -->
<pre><code>[1] &quot;integer&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaXMubnVtZXJpYyhpY2hCaW5JbnRlZ2VyKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">is.numeric</span>(ichBinInteger)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFRSVUVcbiJ9 -->
<pre><code>[1] TRUE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaXMuaW50ZWdlcihpY2hCaW5BdWNoSW50ZWdlcilcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">is.integer</span>(ichBinAuchInteger)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFRSVUVcbiJ9 -->
<pre><code>[1] TRUE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaWNoQmluQnVjaHN0YWJlIDwtIFwiYW55IHN0cmluZ1wiXG5jbGFzcyhpY2hCaW5CdWNoc3RhYmUpXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">ichBinBuchstabe &lt;-<span class="st"> &quot;any string&quot;</span>
<span class="kw">class</span>(ichBinBuchstabe)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiY2hhcmFjdGVyXCJcbiJ9 -->
<pre><code>[1] &quot;character&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubmNoYXIoaWNoQmluQnVjaHN0YWJlKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">nchar</span>(ichBinBuchstabe)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDEwXG4ifQ== -->
<pre><code>[1] 10</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaWNoQmluRGF0dW0gPC0gYXMuRGF0ZShcIjIwMTYtMDItMTcgMDA6MjlcIilcbmljaEJpbkRhdHVtXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">ichBinDatum &lt;-<span class="st"> </span><span class="kw">as.Date</span>(<span class="st">&quot;2016-02-17 00:29&quot;</span>)
ichBinDatum</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiMjAxNi0wMi0xN1wiXG4ifQ== -->
<pre><code>[1] &quot;2016-02-17&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuY2xhc3MoaWNoQmluRGF0dW0pXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">class</span>(ichBinDatum)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiRGF0ZVwiXG4ifQ== -->
<pre><code>[1] &quot;Date&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXMubnVtZXJpYyhpY2hCaW5EYXR1bSlcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">as.numeric</span>(ichBinDatum)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDE2ODQ4XG4ifQ== -->
<pre><code>[1] 16848</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaWNoQmluQXVjaERhdHVtIDwtIGFzLkRhdGUoXCIyMDE2LTAyLTE0IDAwOjI5XCIpXG5pY2hCaW5EYXR1bS1pY2hCaW5BdWNoRGF0dW1cbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">ichBinAuchDatum &lt;-<span class="st"> </span><span class="kw">as.Date</span>(<span class="st">&quot;2016-02-14 00:29&quot;</span>)
ichBinDatum-ichBinAuchDatum</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiVGltZSBkaWZmZXJlbmNlIG9mIDMgZGF5c1xuIn0= -->
<pre><code>Time difference of 3 days</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuY2xhc3MoaWNoQmluRGF0dW0taWNoQmluQXVjaERhdHVtKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">class</span>(ichBinDatum-ichBinAuchDatum)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiZGlmZnRpbWVcIlxuIn0= -->
<pre><code>[1] &quot;difftime&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXMubnVtZXJpYyhpY2hCaW5EYXR1bS1pY2hCaW5BdWNoRGF0dW0pXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">as.numeric</span>(ichBinDatum-ichBinAuchDatum)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDNcbiJ9 -->
<pre><code>[1] 3</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaUFtVHJ1ZSA8LSBUUlVFXG5jbGFzcyhpQW1UcnVlKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">iAmTrue &lt;-<span class="st"> </span><span class="ot">TRUE</span>
<span class="kw">class</span>(iAmTrue)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwibG9naWNhbFwiXG4ifQ== -->
<pre><code>[1] &quot;logical&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaUFtTG9naWNhbCA8LSAyICE9IDNcbmlBbUxvZ2ljYWxcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">iAmLogical &lt;-<span class="st"> </span><span class="dv">2</span> !=<span class="st"> </span><span class="dv">3</span>
iAmLogical</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFRSVUVcbiJ9 -->
<pre><code>[1] TRUE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaUNvbXBhcmVDaGFyYWN0ZXJzIDwtIFwiUmVkXCIgPiBcIkJsdWVcIlxuaUNvbXBhcmVDaGFyYWN0ZXJzXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">iCompareCharacters &lt;-<span class="st"> &quot;Red&quot;</span> &gt;<span class="st"> &quot;Blue&quot;</span>
iCompareCharacters</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFRSVUVcbiJ9 -->
<pre><code>[1] TRUE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-chunk-end -->
<!-- rnb-text-begin -->
</div>
<div id="vektoren-zuweisung-arithmetik-und-indizierung" class="section level2">
<h2>Vektoren: Zuweisung¸ Arithmetik und Indizierung</h2>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuc2ltcGxlU2VxdWVuY2UgPC0gMToxMlxuc2ltcGxlU2VxdWVuY2VcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">simpleSequence &lt;-<span class="st"> </span><span class="dv">1</span>:<span class="dv">12</span>
simpleSequence</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiIFsxXSAgMSAgMiAgMyAgNCAgNSAgNiAgNyAgOCAgOSAxMCAxMSAxMlxuIn0= -->
<pre><code> [1]  1  2  3  4  5  6  7  8  9 10 11 12</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZXZlbk51bWJlclNlcXVlbmNlIDwtIDIqMTo2XG5ldmVuTnVtYmVyU2VxdWVuY2VcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">evenNumberSequence &lt;-<span class="st"> </span><span class="dv">2</span>*<span class="dv">1</span>:<span class="dv">6</span>
evenNumberSequence</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAyICA0ICA2ICA4IDEwIDEyXG4ifQ== -->
<pre><code>[1]  2  4  6  8 10 12</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxucmVwZWF0U2VxdWVuY2UgPC0gcmVwKGV2ZW5OdW1iZXJTZXF1ZW5jZSwgdGltZXMgPSAyLCBsZW5ndGgub3V0ID0gMjAsIGVhY2ggPSAzKVxucmVwZWF0U2VxdWVuY2VcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">repeatSequence &lt;-<span class="st"> </span><span class="kw">rep</span>(evenNumberSequence, <span class="dt">times =</span> <span class="dv">2</span>, <span class="dt">length.out =</span> <span class="dv">20</span>, <span class="dt">each =</span> <span class="dv">3</span>)
repeatSequence</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiIFsxXSAgMiAgMiAgMiAgNCAgNCAgNCAgNiAgNiAgNiAgOCAgOCAgOCAxMCAxMCAxMCAxMiAxMiAxMiAgMiAgMlxuIn0= -->
<pre><code> [1]  2  2  2  4  4  4  6  6  6  8  8  8 10 10 10 12 12 12  2  2</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZ2VuZXJhbFNlcXVlbmNlIDwtIHNlcShmcm9tID0gLTUsIHRvID0gMTAsIGJ5ID0gMC4yKVxuZ2VuZXJhbFNlcXVlbmNlXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">generalSequence &lt;-<span class="st"> </span><span class="kw">seq</span>(<span class="dt">from =</span> -<span class="dv">5</span>, <span class="dt">to =</span> <span class="dv">10</span>, <span class="dt">by =</span> <span class="fl">0.2</span>)
generalSequence</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiIFsxXSAtNS4wIC00LjggLTQuNiAtNC40IC00LjIgLTQuMCAtMy44IC0zLjYgLTMuNCAtMy4yIC0zLjAgLTIuOCAtMi42IC0yLjQgLTIuMiAtMi4wIC0xLjggLTEuNiAtMS40IC0xLjIgLTEuMCAtMC44IC0wLjYgLTAuNCAtMC4yXG5bMjZdICAwLjAgIDAuMiAgMC40ICAwLjYgIDAuOCAgMS4wICAxLjIgIDEuNCAgMS42ICAxLjggIDIuMCAgMi4yICAyLjQgIDIuNiAgMi44ICAzLjAgIDMuMiAgMy40ICAzLjYgIDMuOCAgNC4wICA0LjIgIDQuNCAgNC42ICA0Ljhcbls1MV0gIDUuMCAgNS4yICA1LjQgIDUuNiAgNS44ICA2LjAgIDYuMiAgNi40ICA2LjYgIDYuOCAgNy4wICA3LjIgIDcuNCAgNy42ICA3LjggIDguMCAgOC4yICA4LjQgIDguNiAgOC44ICA5LjAgIDkuMiAgOS40ICA5LjYgIDkuOFxuWzc2XSAxMC4wXG4ifQ== -->
<pre><code> [1] -5.0 -4.8 -4.6 -4.4 -4.2 -4.0 -3.8 -3.6 -3.4 -3.2 -3.0 -2.8 -2.6 -2.4 -2.2 -2.0 -1.8 -1.6 -1.4 -1.2 -1.0 -0.8 -0.6 -0.4 -0.2
[26]  0.0  0.2  0.4  0.6  0.8  1.0  1.2  1.4  1.6  1.8  2.0  2.2  2.4  2.6  2.8  3.0  3.2  3.4  3.6  3.8  4.0  4.2  4.4  4.6  4.8
[51]  5.0  5.2  5.4  5.6  5.8  6.0  6.2  6.4  6.6  6.8  7.0  7.2  7.4  7.6  7.8  8.0  8.2  8.4  8.6  8.8  9.0  9.2  9.4  9.6  9.8
[76] 10.0</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjMSA8LSBjKDI0NywgMzUwLCBcIlRlc3RcIiwgVFJVRSwgNjAwKVxubW9kZSh2ZWMxKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">vec1 &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="dv">247</span>, <span class="dv">350</span>, <span class="st">&quot;Test&quot;</span>, <span class="ot">TRUE</span>, <span class="dv">600</span>)
<span class="kw">mode</span>(vec1)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiY2hhcmFjdGVyXCJcbiJ9 -->
<pre><code>[1] &quot;character&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudHlwZW9mKHZlYzEpXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">typeof</span>(vec1)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiY2hhcmFjdGVyXCJcbiJ9 -->
<pre><code>[1] &quot;character&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjMiA8LSBudW1lcmljKDUpXG52ZWMyXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">vec2 &lt;-<span class="st"> </span><span class="kw">numeric</span>(<span class="dv">5</span>)
vec2</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDAgMCAwIDAgMFxuIn0= -->
<pre><code>[1] 0 0 0 0 0</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjMyA8LSBjKHZlYzIsIHZlYzEpXG52ZWMzXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">vec3 &lt;-<span class="st"> </span><span class="kw">c</span>(vec2, vec1)
vec3</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiIFsxXSBcIjBcIiAgICBcIjBcIiAgICBcIjBcIiAgICBcIjBcIiAgICBcIjBcIiAgICBcIjI0N1wiICBcIjM1MFwiICBcIlRlc3RcIiBcIlRSVUVcIiBcIjYwMFwiIFxuIn0= -->
<pre><code> [1] &quot;0&quot;    &quot;0&quot;    &quot;0&quot;    &quot;0&quot;    &quot;0&quot;    &quot;247&quot;  &quot;350&quot;  &quot;Test&quot; &quot;TRUE&quot; &quot;600&quot; </code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjMTAgPC0gYygxLCA1LCAxMCwgMjAsIDUwLCAxMDAsIDUwMClcbnZlYzIwIDwtIGMoMCwgMzApXG5mb3IoaSBpbiB2ZWMxMCkge1xuICB2ZWMyMCA8LSBjKHZlYzIwICwgaSozMClcbn1cbnZlYzIwXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">vec10 &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="dv">1</span>, <span class="dv">5</span>, <span class="dv">10</span>, <span class="dv">20</span>, <span class="dv">50</span>, <span class="dv">100</span>, <span class="dv">500</span>)
vec20 &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="dv">0</span>, <span class="dv">30</span>)
for(i in vec10) {
  vec20 &lt;-<span class="st"> </span><span class="kw">c</span>(vec20 , i*<span class="dv">30</span>)
}
vec20</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAgICAwICAgIDMwICAgIDMwICAgMTUwICAgMzAwICAgNjAwICAxNTAwICAzMDAwIDE1MDAwXG4ifQ== -->
<pre><code>[1]     0    30    30   150   300   600  1500  3000 15000</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjMzAgPC0gYyg1LCA1LCA1LCA2LCAyLCAyLCAyKVxudmVjNDAgPC0gdmVjMzAgKiB2ZWMxMFxudmVjNDBcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">vec30 &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="dv">5</span>, <span class="dv">5</span>, <span class="dv">5</span>, <span class="dv">6</span>, <span class="dv">2</span>, <span class="dv">2</span>, <span class="dv">2</span>)
vec40 &lt;-<span class="st"> </span>vec30 *<span class="st"> </span>vec10
vec40</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAgIDUgICAyNSAgIDUwICAxMjAgIDEwMCAgMjAwIDEwMDBcbiJ9 -->
<pre><code>[1]    5   25   50  120  100  200 1000</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjNTAgPC0gdmVjNDAgKyBjKDEwMCwwKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">vec50 &lt;-<span class="st"> </span>vec40 +<span class="st"> </span><span class="kw">c</span>(<span class="dv">100</span>,<span class="dv">0</span>)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiTMOkbmdlIGRlcyBsw6RuZ2VyZW4gT2JqZWt0ZXNcbiBcdCBpc3Qga2VpbiBWaWVsZmFjaGVzIGRlciBMw6RuZ2UgZGVzIGvDvHJ6ZXJlbiBPYmpla3Rlc1xuIn0= -->
<pre><code>Länge des längeren Objektes
     ist kein Vielfaches der Länge des kürzeren Objektes</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjNTBcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">vec50</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAxMDUgICAyNSAgMTUwICAxMjAgIDIwMCAgMjAwIDExMDBcbiJ9 -->
<pre><code>[1]  105   25  150  120  200  200 1100</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuc2VxMSA8LSAxOjRcbnNlcTEgPT0gMlxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">seq1 &lt;-<span class="st"> </span><span class="dv">1</span>:<span class="dv">4</span>
seq1 ==<span class="st"> </span><span class="dv">2</span></code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIEZBTFNFICBUUlVFIEZBTFNFIEZBTFNFXG4ifQ== -->
<pre><code>[1] FALSE  TRUE FALSE FALSE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuc3RyaW5nU2VxIDwtIGMoXCJBXCIsIFwiQlwiLCBcIkNcIiwgXCJEXCIsIFwiRVwiLCBcIkZcIiwgXCJHXCIsIFwiSFwiKVxuZnVua3lTZXEgPC0gcGFzdGUoc3RyaW5nU2VxLCBzZXExLCBzZXA9XCJcIilcbmZ1bmt5U2VxXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">stringSeq &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;A&quot;</span>, <span class="st">&quot;B&quot;</span>, <span class="st">&quot;C&quot;</span>, <span class="st">&quot;D&quot;</span>, <span class="st">&quot;E&quot;</span>, <span class="st">&quot;F&quot;</span>, <span class="st">&quot;G&quot;</span>, <span class="st">&quot;H&quot;</span>)
funkySeq &lt;-<span class="st"> </span><span class="kw">paste</span>(stringSeq, seq1, <span class="dt">sep=</span><span class="st">&quot;&quot;</span>)
funkySeq</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiQTFcIiBcIkIyXCIgXCJDM1wiIFwiRDRcIiBcIkUxXCIgXCJGMlwiIFwiRzNcIiBcIkg0XCJcbiJ9 -->
<pre><code>[1] &quot;A1&quot; &quot;B2&quot; &quot;C3&quot; &quot;D4&quot; &quot;E1&quot; &quot;F2&quot; &quot;G3&quot; &quot;H4&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubWVpbmVTZXEgPC0gMyoxOjVcbm1laW5lU2VxW3JlcChjKDEsMyksIHRpbWVzID0gNSldXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">meineSeq &lt;-<span class="st"> </span><span class="dv">3</span>*<span class="dv">1</span>:<span class="dv">5</span>
meineSeq[<span class="kw">rep</span>(<span class="kw">c</span>(<span class="dv">1</span>,<span class="dv">3</span>), <span class="dt">times =</span> <span class="dv">5</span>)]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiIFsxXSAzIDkgMyA5IDMgOSAzIDkgMyA5XG4ifQ== -->
<pre><code> [1] 3 9 3 9 3 9 3 9 3 9</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubWVpbmVTZXFbYygtMywgLTQpXVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">meineSeq[<span class="kw">c</span>(-<span class="dv">3</span>, -<span class="dv">4</span>)]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAzICA2IDE1XG4ifQ== -->
<pre><code>[1]  3  6 15</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubmFtZXMobWVpbmVTZXEpIDwtIGMoXCJBXCIsXCJCXCIsXCJDXCIsXCJEXCIsXCJFXCIpXG5tZWluZVNlcVtjKFwiQVwiLFwiQ1wiKV1cbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">names</span>(meineSeq) &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;A&quot;</span>,<span class="st">&quot;B&quot;</span>,<span class="st">&quot;C&quot;</span>,<span class="st">&quot;D&quot;</span>,<span class="st">&quot;E&quot;</span>)
meineSeq[<span class="kw">c</span>(<span class="st">&quot;A&quot;</span>,<span class="st">&quot;C&quot;</span>)]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiQSBDIFxuMyA5IFxuIn0= -->
<pre><code>A C 
3 9 </code></pre>
<!-- rnb-output-end -->
<!-- rnb-chunk-end -->
<!-- rnb-text-begin -->
</div>
<div id="arrays" class="section level2">
<h2>Arrays</h2>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMSA8LSBhcnJheShjKDE6MTIpLCBkaW0gPSBjKDMsMiwyKSlcbmFycjFcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">arr1 &lt;-<span class="st"> </span><span class="kw">array</span>(<span class="kw">c</span>(<span class="dv">1</span>:<span class="dv">12</span>), <span class="dt">dim =</span> <span class="kw">c</span>(<span class="dv">3</span>,<span class="dv">2</span>,<span class="dv">2</span>))
arr1</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiLCAsIDFcblxuICAgICBbLDFdIFssMl1cblsxLF0gICAgMSAgICA0XG5bMixdICAgIDIgICAgNVxuWzMsXSAgICAzICAgIDZcblxuLCAsIDJcblxuICAgICBbLDFdIFssMl1cblsxLF0gICAgNyAgIDEwXG5bMixdICAgIDggICAxMVxuWzMsXSAgICA5ICAgMTJcbiJ9 -->
<pre><code>, , 1

     [,1] [,2]
[1,]    1    4
[2,]    2    5
[3,]    3    6

, , 2

     [,1] [,2]
[1,]    7   10
[2,]    8   11
[3,]    9   12</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMiA8LSBhcnJheShjKDEsMCkgLCBkaW0gPSBjKDIsMykpXG5hcnIyXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">arr2 &lt;-<span class="st"> </span><span class="kw">array</span>(<span class="kw">c</span>(<span class="dv">1</span>,<span class="dv">0</span>) , <span class="dt">dim =</span> <span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>))
arr2</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgICAxICAgIDEgICAgMVxuWzIsXSAgICAwICAgIDAgICAgMFxuIn0= -->
<pre><code>     [,1] [,2] [,3]
[1,]    1    1    1
[2,]    0    0    0</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMVsyLDIsMV1cbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">arr1[<span class="dv">2</span>,<span class="dv">2</span>,<span class="dv">1</span>]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDVcbiJ9 -->
<pre><code>[1] 5</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMVsyOjMsLDFdXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">arr1[<span class="dv">2</span>:<span class="dv">3</span>,,<span class="dv">1</span>]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl1cblsxLF0gICAgMiAgICA1XG5bMixdICAgIDMgICAgNlxuIn0= -->
<pre><code>     [,1] [,2]
[1,]    2    5
[2,]    3    6</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaW5kZXhBcnJheSA8LSBhcnJheSAoYygxOjIpLCBkaW09YygyLDMpKVxuaW5kZXhBcnJheVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">indexArray &lt;-<span class="st"> </span><span class="kw">array</span> (<span class="kw">c</span>(<span class="dv">1</span>:<span class="dv">2</span>), <span class="dt">dim=</span><span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>))
indexArray</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgICAxICAgIDEgICAgMVxuWzIsXSAgICAyICAgIDIgICAgMlxuIn0= -->
<pre><code>     [,1] [,2] [,3]
[1,]    1    1    1
[2,]    2    2    2</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMVtpbmRleEFycmF5XVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">arr1[indexArray]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAxIDExXG4ifQ== -->
<pre><code>[1]  1 11</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaW5kZXgyQXJyYXkgPC0gYXJyYXkgKGMoMiwzLDIsMSwxLDIpLCBkaW09YygyLDMpKVxuaW5kZXgyQXJyYXlcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">index2Array &lt;-<span class="st"> </span><span class="kw">array</span> (<span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>,<span class="dv">2</span>,<span class="dv">1</span>,<span class="dv">1</span>,<span class="dv">2</span>), <span class="dt">dim=</span><span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>))
index2Array</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgICAyICAgIDIgICAgMVxuWzIsXSAgICAzICAgIDEgICAgMlxuIn0= -->
<pre><code>     [,1] [,2] [,3]
[1,]    2    2    1
[2,]    3    1    2</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMVtpbmRleDJBcnJheV1cbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">arr1[index2Array]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDUgOVxuIn0= -->
<pre><code>[1] 5 9</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYSA8LSBhcnJheSgxOjYsIGRpbSA9IGMoMiwzKSlcbmIgPC0gYXJyYXkoNzoxMiwgZGltID0gYygyLDMpKVxuYSAqIGJcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">a &lt;-<span class="st"> </span><span class="kw">array</span>(<span class="dv">1</span>:<span class="dv">6</span>, <span class="dt">dim =</span> <span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>))
b &lt;-<span class="st"> </span><span class="kw">array</span>(<span class="dv">7</span>:<span class="dv">12</span>, <span class="dt">dim =</span> <span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>))
a *<span class="st"> </span>b</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgICA3ICAgMjcgICA1NVxuWzIsXSAgIDE2ICAgNDAgICA3MlxuIn0= -->
<pre><code>     [,1] [,2] [,3]
[1,]    7   27   55
[2,]   16   40   72</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuIyBvdXRlciBwcm9kdWN0XG5BIDwtIGFycmF5KDE6MTgsIGRpbSA9IGMoMywyLDMpKVxuQiA8LSBhcnJheSgxOTozNiwgZGltID0gYygyLDMsMykpXG5BXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="co"># outer product</span>
A &lt;-<span class="st"> </span><span class="kw">array</span>(<span class="dv">1</span>:<span class="dv">18</span>, <span class="dt">dim =</span> <span class="kw">c</span>(<span class="dv">3</span>,<span class="dv">2</span>,<span class="dv">3</span>))
B &lt;-<span class="st"> </span><span class="kw">array</span>(<span class="dv">19</span>:<span class="dv">36</span>, <span class="dt">dim =</span> <span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>,<span class="dv">3</span>))
A</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiLCAsIDFcblxuICAgICBbLDFdIFssMl1cblsxLF0gICAgMSAgICA0XG5bMixdICAgIDIgICAgNVxuWzMsXSAgICAzICAgIDZcblxuLCAsIDJcblxuICAgICBbLDFdIFssMl1cblsxLF0gICAgNyAgIDEwXG5bMixdICAgIDggICAxMVxuWzMsXSAgICA5ICAgMTJcblxuLCAsIDNcblxuICAgICBbLDFdIFssMl1cblsxLF0gICAxMyAgIDE2XG5bMixdICAgMTQgICAxN1xuWzMsXSAgIDE1ICAgMThcbiJ9 -->
<pre><code>, , 1

     [,1] [,2]
[1,]    1    4
[2,]    2    5
[3,]    3    6

, , 2

     [,1] [,2]
[1,]    7   10
[2,]    8   11
[3,]    9   12

, , 3

     [,1] [,2]
[1,]   13   16
[2,]   14   17
[3,]   15   18</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuQlxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">B</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiLCAsIDFcblxuICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgIDE5ICAgMjEgICAyM1xuWzIsXSAgIDIwICAgMjIgICAyNFxuXG4sICwgMlxuXG4gICAgIFssMV0gWywyXSBbLDNdXG5bMSxdICAgMjUgICAyNyAgIDI5XG5bMixdICAgMjYgICAyOCAgIDMwXG5cbiwgLCAzXG5cbiAgICAgWywxXSBbLDJdIFssM11cblsxLF0gICAzMSAgIDMzICAgMzVcblsyLF0gICAzMiAgIDM0ICAgMzZcbiJ9 -->
<pre><code>, , 1

     [,1] [,2] [,3]
[1,]   19   21   23
[2,]   20   22   24

, , 2

     [,1] [,2] [,3]
[1,]   25   27   29
[2,]   26   28   30

, , 3

     [,1] [,2] [,3]
[1,]   31   33   35
[2,]   32   34   36</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuQUIgPC0gQSAlbyUgQlxuZGltKEFCKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">AB &lt;-<span class="st"> </span>A %o%<span class="st"> </span>B
<span class="kw">dim</span>(AB)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDMgMiAzIDIgMyAzXG4ifQ== -->
<pre><code>[1] 3 2 3 2 3 3</code></pre>
<!-- rnb-output-end -->
<!-- rnb-chunk-end -->
<!-- rnb-text-begin -->
</div>
<div id="matrizen" class="section level2">
<h2>Matrizen</h2>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYU1hdHJpeCA8LSBtYXRyaXgoYygyKjE6MywgMyoxOjMpLCBucm93ID0gMiwgbmNvbCA9IDMpXG5hTWF0cml4XG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">aMatrix &lt;-<span class="st"> </span><span class="kw">matrix</span>(<span class="kw">c</span>(<span class="dv">2</span>*<span class="dv">1</span>:<span class="dv">3</span>, <span class="dv">3</span>*<span class="dv">1</span>:<span class="dv">3</span>), <span class="dt">nrow =</span> <span class="dv">2</span>, <span class="dt">ncol =</span> <span class="dv">3</span>)
aMatrix</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgICAyICAgIDYgICAgNlxuWzIsXSAgICA0ICAgIDMgICAgOVxuIn0= -->
<pre><code>     [,1] [,2] [,3]
[1,]    2    6    6
[2,]    4    3    9</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuIyBUcmFuc3BvbmllcmVuXG5hbm90aGVyTWF0cml4IDwtIHQoYU1hdHJpeClcbiMgTWF0cml6ZW5tdWx0aXBsaWthdGlvblxuYU1hdHJpeCAlKiUgYW5vdGhlck1hdHJpeCBcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="co"># Transponieren</span>
anotherMatrix &lt;-<span class="st"> </span><span class="kw">t</span>(aMatrix)
<span class="co"># Matrizenmultiplikation</span>
aMatrix %*%<span class="st"> </span>anotherMatrix </code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl1cblsxLF0gICA3NiAgIDgwXG5bMixdICAgODAgIDEwNlxuIn0= -->
<pre><code>     [,1] [,2]
[1,]   76   80
[2,]   80  106</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuIyBLcmV1enByb2R1a3Qgdm9uIEEsIEIgPT0gdChBKSAlKiUgQlxuY3Jvc3Nwcm9kKGFNYXRyaXgsMioxOjIpXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="co"># Kreuzprodukt von A, B == t(A) %*% B</span>
<span class="kw">crossprod</span>(aMatrix,<span class="dv">2</span>*<span class="dv">1</span>:<span class="dv">2</span>)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdXG5bMSxdICAgMjBcblsyLF0gICAyNFxuWzMsXSAgIDQ4XG4ifQ== -->
<pre><code>     [,1]
[1,]   20
[2,]   24
[3,]   48</code></pre>
<!-- rnb-output-end -->
<!-- rnb-chunk-end -->
<!-- rnb-text-begin -->
</div>
<div id="faktoren" class="section level2">
<h2>Faktoren</h2>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuc3RhZHQgPC0gYyhcIkJlcmxpblwiLCBcIkRyZXNkZW5cIiwgXCJIYW1idXJnXCIsIFwiQmVybGluXCIsIFwiQmVybGluXCIsIFwiSGFtYnVyZ1wiLCBcIkRyZXNkZW5cIilcbmthdGVnb3JpZSA8LSBjKFwiQmVrbGVpZHVuZ1wiLCBcIlNjaHVoZVwiLCBcIktvc21ldGlrXCIsIFwiS29zbWV0aWtcIiwgXCJTY2h1aGVcIiwgXCJCZWtsZWlkdW5nXCIsIFwiQmVrbGVpZHVuZ1wiKVxuYmV0cmFnIDwtIGMoNTAwMCwgNDUwMCwgMzUwMCwgMjUwMCwgMTAwMCwgMjAwMCwgNTUwMClcbnN0YWR0QXNGYWt0b3IgPC0gZmFjdG9yKHN0YWR0KVxucHJpbnQoc3RhZHRBc0Zha3RvcilcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">stadt &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;Berlin&quot;</span>, <span class="st">&quot;Dresden&quot;</span>, <span class="st">&quot;Hamburg&quot;</span>, <span class="st">&quot;Berlin&quot;</span>, <span class="st">&quot;Berlin&quot;</span>, <span class="st">&quot;Hamburg&quot;</span>, <span class="st">&quot;Dresden&quot;</span>)
kategorie &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;Bekleidung&quot;</span>, <span class="st">&quot;Schuhe&quot;</span>, <span class="st">&quot;Kosmetik&quot;</span>, <span class="st">&quot;Kosmetik&quot;</span>, <span class="st">&quot;Schuhe&quot;</span>, <span class="st">&quot;Bekleidung&quot;</span>, <span class="st">&quot;Bekleidung&quot;</span>)
betrag &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="dv">5000</span>, <span class="dv">4500</span>, <span class="dv">3500</span>, <span class="dv">2500</span>, <span class="dv">1000</span>, <span class="dv">2000</span>, <span class="dv">5500</span>)
stadtAsFaktor &lt;-<span class="st"> </span><span class="kw">factor</span>(stadt)
<span class="kw">print</span>(stadtAsFaktor)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIEJlcmxpbiAgRHJlc2RlbiBIYW1idXJnIEJlcmxpbiAgQmVybGluICBIYW1idXJnIERyZXNkZW5cbkxldmVsczogQmVybGluIERyZXNkZW4gSGFtYnVyZ1xuIn0= -->
<pre><code>[1] Berlin  Dresden Hamburg Berlin  Berlin  Hamburg Dresden
Levels: Berlin Dresden Hamburg</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXMubnVtZXJpYyhzdGFkdEFzRmFrdG9yKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">as.numeric</span>(stadtAsFaktor)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDEgMiAzIDEgMSAzIDJcbiJ9 -->
<pre><code>[1] 1 2 3 1 1 3 2</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubGV2ZWxzKHN0YWR0QXNGYWt0b3IpXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">levels</span>(stadtAsFaktor)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiQmVybGluXCIgIFwiRHJlc2RlblwiIFwiSGFtYnVyZ1wiXG4ifQ== -->
<pre><code>[1] &quot;Berlin&quot;  &quot;Dresden&quot; &quot;Hamburg&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubGV2ZWxzKHN0YWR0QXNGYWt0b3IpIDwtIGMoXCJCRVJcIiwgXCJEUkVcIiwgXCJIQU1cIilcbnN0YWR0Q29kZUZha3RvciA8LSBmYWN0b3Ioc3RhZHRBc0Zha3RvciwgbGFiZWxzPWMoXCJCXCIsIFwiRFwiLCBcIkhcIikpXG5wcmludChzdGFkdENvZGVGYWt0b3IpXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">levels</span>(stadtAsFaktor) &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;BER&quot;</span>, <span class="st">&quot;DRE&quot;</span>, <span class="st">&quot;HAM&quot;</span>)
stadtCodeFaktor &lt;-<span class="st"> </span><span class="kw">factor</span>(stadtAsFaktor, <span class="dt">labels=</span><span class="kw">c</span>(<span class="st">&quot;B&quot;</span>, <span class="st">&quot;D&quot;</span>, <span class="st">&quot;H&quot;</span>))
<span class="kw">print</span>(stadtCodeFaktor)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIEIgRCBIIEIgQiBIIERcbkxldmVsczogQiBEIEhcbiJ9 -->
<pre><code>[1] B D H B B H D
Levels: B D H</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudGFibGUoc3RhZHQpXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">table</span>(stadt)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoic3RhZHRcbiBCZXJsaW4gRHJlc2RlbiBIYW1idXJnIFxuICAgICAgMyAgICAgICAyICAgICAgIDIgXG4ifQ== -->
<pre><code>stadt
 Berlin Dresden Hamburg 
      3       2       2 </code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudGFwcGx5KGJldHJhZywga2F0ZWdvcmllLCBzdW0pXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">tapply</span>(betrag, kategorie, sum)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiQmVrbGVpZHVuZyAgIEtvc21ldGlrICAgICBTY2h1aGUgXG4gICAgIDEyNTAwICAgICAgIDYwMDAgICAgICAgNTUwMCBcbiJ9 -->
<pre><code>Bekleidung   Kosmetik     Schuhe 
     12500       6000       5500 </code></pre>
<!-- rnb-output-end -->
<!-- rnb-chunk-end -->
<!-- rnb-text-begin -->
<!-- rnb-text-end -->
</div>

<div id="rmd-source-code">LS0tCnRpdGxlOiAiUiBTdGFydGVyIgpvdXRwdXQ6CiAgaHRtbF9ub3RlYm9vazoKICAgIGNvZGVfZm9sZGluZzogbm9uZQogICAgZGZfcHJpbnQ6IGthYmxlCiAgICBoaWdobGlnaHQ6IHB5Z21lbnRzCiAgICB0aGVtZTogZmxhdGx5CiAgaHRtbF9kb2N1bWVudDoKICAgIGhpZ2hsaWdodDogcHlnbWVudHMKICAgIGtlZXBfbWQ6IHllcwotLS0KCiMjIFIgbGVybmVuCgpJY2ggYmluIGJlaSBYREEgYXVmIGVpbmlnZSBPbmxpbmUgS3Vyc2Ugw7xiZXIgTWFjaGluZSBMZWFybmluZyBnZXN0b8OfZW4uIFVuZCBkYSBpY2ggZGFyw7xiZXIgc2Nob24gaW1tZXIgbWVociB3aXNzZW4gd29sbHRlIHVuZCBuZXVlciBLb3BmLUlucHV0IGdlcmFkZSBhbnN0YW5kLCBoYWJlIGljaCBhbmdlZmFuZ2VuIGRlbiBLdXJzIHp1IHNjaGF1ZW4uIEljaCBlcmlubmVydGUgbWljaCBhdcOfZXJkZW0sIHfDpGhyZW5kIGRlcyBVUyBXYWhsa2FtcGZzIGRpZXNlbiBzcGFubmVuZGVuIEFydGlrZWwgW1RleHQgYW5hbHlzaXMgb2YgVHJ1bXAncyB0d2VldHMgY29uZmlybXMgaGUgd3JpdGVzIG9ubHkgdGhlIChhbmdyaWVyKSBBbmRyb2lkIGhhbGZde2h0dHA6Ly92YXJpYW5jZWV4cGxhaW5lZC5vcmcvci90cnVtcC10d2VldHMvfSg6dGFyZ2V0PSJfYmxhbmsiKSBnZWxlc2VuIHp1IGhhYmVuLiBEYXMgd29sbHRlIGljaCBhdWNoIGvDtm5uZW4uIEFsc28gd2FyIGVzIGFuIGRlciBaZWl0LCBkYXMgZ2FueiBhbHRlIFN0YXRpc3Rpay1XaXNzZW4genUgcmVhbmltaWVyZW4gdW5kIGVpbnp1c3RlaWdlbi4gRGVyIEFydGlrZWwgaXN0IG51ciBlaW5lIFNhbW1sdW5nIGRlciBlcnN0ZW4gVHV0b3JpYWxzIMO8YmVyIGRpZSBHcnVuZGxhZ2VuIHZvbiBSIC0tIFZhcmlhYmxlbiwgRWluLSB1bmQgQXVzZ2FiZSwgT3BlcmF0aW9uZW4uIEVpZ2VubGljaCBmw7xyIG1pY2ggYWxzIFdpZWRlcmhvbHVuZyBnZXNjaHJpZWJlbi4gVmllbGxlaWNodCBrcmllZ3QgamEgbm9jaCBqZW1hbmQgbHVzdCwgUiBhdXN6dXByb2JpZXJlbi4gCkFsbGVzIHdpciBoZXV0ZSBtaXQgVG9ydGVuIHVuZCBCYWxrZW4gYmVncsO8bmRldCB1bmQgd2lyICtnbGF1YmVuKywgc29iYWxkIHdpciBlaW5lIGJlZ3LDvG5kZXRlIEdyYWZpayBzZWhlbi4gSWNoIGRlbmtlLCBtYW4gc29sbHRlIHNpZSBhdWNoIHNlbGJzdCBoZXJzdGVsbGVuIGvDtm5uZW4uCgojIyBWYXJpYWJsZW46IFp1d2Vpc3VuZyB1bmQgQXVzZ2FiZQoKRGllIGVyc3RlbiBTY2hyaXR0ZSBpbSBVbWdhbmcgbWl0IGV0d2FzIE5ldWVtIHNvbGx0ZW4gaW1tZXIgYmVnaW5uZW4gbWl0OiBXaWUgbWFjaGUgaWNoIGVzIGFuLCB3aWUgbWFjaGUgaWNoIGVzIGF1cy4gQmVpIGVpbmVyIFByb2dyYW1tbWllcnNwcmFjaGUgd8OkcmUgZGFzIGRhbm46IFdpZSBnZWJlIGljaCBldHdhcyBlaW4sIHdpZSBnZWJlIGljaCBldHdhcyBhdXMuIFVuZCB6dW0gQXVzZ2ViZW4gYnJhdWNodCBtYW4gZWluIERpbmcgZ2VuYW5udCBWYXJpYWJsZS4gRGFoZXIgZmFuZ2UgaWNoIGRhbWl0IGFuLiBXaWUgd2VyZGVuIFZhcmlhYmxlbiBpbml0aWFsaXNpZXJ0LCB3aWUgd2Vpc2UgaWNoIGlobmVuIGVpbmVuIFdlcnQgenUgdW5kIHdpZSBnZWJlIGljaCBzaWUgZGFubiBhdXMuCkFscyBlcnN0ZXMgZGllIEluaXRhbGlzaWVydW5nIHZvbiBWYXJpYWJsZW4gdW5kIGRpZSBXZXJ0ZXp1d2Vpc3VuZyBtaXQgPSwgLT4gb2RlciA8LS4gVW5kIG5hdMO8cmxpY2ggZGVyZW4gQXVzZ2FiZS4KCmBgYHtyfQplaW5lVmFyaWFibGUgPSAzMgphbmRlcmVWYXJpYWJsZSA8LSAyNwoxOC43IC0+IGRyaXR0ZVZhcmlhYmxlCmVpbmVWYXJpYWJsZQphbmRlcmVWYXJpYWJsZQpkcml0dGVWYXJpYWJsZQplaW5lVmFyaWFibGUKZWluZVZhcmlhYmxlICsgYW5kZXJlVmFyaWFibGUKcHJpbnQoZHJpdHRlVmFyaWFibGUpCmZpcnN0VmFyIDwtIHNlY29uZFZhciA8LSAia29taXNjaCIKY2F0KGZpcnN0VmFyLCAiLCIsIHNlY29uZFZhciwgIiAtIHNpbmQgYmVpZGUgZ2xlaWNoIC0iLCBzZXAgPSAiICIpCmFNZXNzYWdlID0gcGFzdGUoZmlyc3RWYXIsICItIiwiZGFzIGlzdCBkYXNzZWxiZSB3aWUiLCBzZWNvbmRWYXIsIHNlcCA9ICIgIikKbWVzc2FnZShhTWVzc2FnZSkKYGBgCgojIyBEYXRlbnR5cGVuCgoKCmBgYHtyfQppY2hCaW5JbnRlZ2VyIDwtIDRMCmlzLmludGVnZXIoaWNoQmluSW50ZWdlcikKaWNoQmluQXVjaEludGVnZXIgPC0gYXMuaW50ZWdlcigzKzUpCmNsYXNzKGljaEJpbkF1Y2hJbnRlZ2VyKQppcy5udW1lcmljKGljaEJpbkludGVnZXIpCmlzLmludGVnZXIoaWNoQmluQXVjaEludGVnZXIpCmljaEJpbkJ1Y2hzdGFiZSA8LSAiYW55IHN0cmluZyIKY2xhc3MoaWNoQmluQnVjaHN0YWJlKQpuY2hhcihpY2hCaW5CdWNoc3RhYmUpCmljaEJpbkRhdHVtIDwtIGFzLkRhdGUoIjIwMTYtMDItMTcgMDA6MjkiKQppY2hCaW5EYXR1bQpjbGFzcyhpY2hCaW5EYXR1bSkKYXMubnVtZXJpYyhpY2hCaW5EYXR1bSkKaWNoQmluQXVjaERhdHVtIDwtIGFzLkRhdGUoIjIwMTYtMDItMTQgMDA6MjkiKQppY2hCaW5EYXR1bS1pY2hCaW5BdWNoRGF0dW0KY2xhc3MoaWNoQmluRGF0dW0taWNoQmluQXVjaERhdHVtKQphcy5udW1lcmljKGljaEJpbkRhdHVtLWljaEJpbkF1Y2hEYXR1bSkKaUFtVHJ1ZSA8LSBUUlVFCmNsYXNzKGlBbVRydWUpCmlBbUxvZ2ljYWwgPC0gMiAhPSAzCmlBbUxvZ2ljYWwKaUNvbXBhcmVDaGFyYWN0ZXJzIDwtICJSZWQiID4gIkJsdWUiCmlDb21wYXJlQ2hhcmFjdGVycwpgYGAKCiMjIFZla3RvcmVuOiBadXdlaXN1bmfCuCBBcml0aG1ldGlrIHVuZCBJbmRpemllcnVuZwoKCmBgYHtyfQpzaW1wbGVTZXF1ZW5jZSA8LSAxOjEyCnNpbXBsZVNlcXVlbmNlCmV2ZW5OdW1iZXJTZXF1ZW5jZSA8LSAyKjE6NgpldmVuTnVtYmVyU2VxdWVuY2UKcmVwZWF0U2VxdWVuY2UgPC0gcmVwKGV2ZW5OdW1iZXJTZXF1ZW5jZSwgdGltZXMgPSAyLCBsZW5ndGgub3V0ID0gMjAsIGVhY2ggPSAzKQpyZXBlYXRTZXF1ZW5jZQpnZW5lcmFsU2VxdWVuY2UgPC0gc2VxKGZyb20gPSAtNSwgdG8gPSAxMCwgYnkgPSAwLjIpCmdlbmVyYWxTZXF1ZW5jZQp2ZWMxIDwtIGMoMjQ3LCAzNTAsICJUZXN0IiwgVFJVRSwgNjAwKQptb2RlKHZlYzEpCnR5cGVvZih2ZWMxKQp2ZWMyIDwtIG51bWVyaWMoNSkKdmVjMgp2ZWMzIDwtIGModmVjMiwgdmVjMSkKdmVjMwp2ZWMxMCA8LSBjKDEsIDUsIDEwLCAyMCwgNTAsIDEwMCwgNTAwKQp2ZWMyMCA8LSBjKDAsIDMwKQpmb3IoaSBpbiB2ZWMxMCkgewogIHZlYzIwIDwtIGModmVjMjAgLCBpKjMwKQp9CnZlYzIwCnZlYzMwIDwtIGMoNSwgNSwgNSwgNiwgMiwgMiwgMikKdmVjNDAgPC0gdmVjMzAgKiB2ZWMxMAp2ZWM0MAp2ZWM1MCA8LSB2ZWM0MCArIGMoMTAwLDApCnZlYzUwCnNlcTEgPC0gMTo0CnNlcTEgPT0gMgpzdHJpbmdTZXEgPC0gYygiQSIsICJCIiwgIkMiLCAiRCIsICJFIiwgIkYiLCAiRyIsICJIIikKZnVua3lTZXEgPC0gcGFzdGUoc3RyaW5nU2VxLCBzZXExLCBzZXA9IiIpCmZ1bmt5U2VxCm1laW5lU2VxIDwtIDMqMTo1Cm1laW5lU2VxW3JlcChjKDEsMyksIHRpbWVzID0gNSldCm1laW5lU2VxW2MoLTMsIC00KV0KbmFtZXMobWVpbmVTZXEpIDwtIGMoIkEiLCJCIiwiQyIsIkQiLCJFIikKbWVpbmVTZXFbYygiQSIsIkMiKV0KYGBgCgojIyBBcnJheXMKCmBgYHtyfQphcnIxIDwtIGFycmF5KGMoMToxMiksIGRpbSA9IGMoMywyLDIpKQphcnIxCmFycjIgPC0gYXJyYXkoYygxLDApICwgZGltID0gYygyLDMpKQphcnIyCmFycjFbMiwyLDFdCmFycjFbMjozLCwxXQppbmRleEFycmF5IDwtIGFycmF5IChjKDE6MiksIGRpbT1jKDIsMykpCmluZGV4QXJyYXkKYXJyMVtpbmRleEFycmF5XQppbmRleDJBcnJheSA8LSBhcnJheSAoYygyLDMsMiwxLDEsMiksIGRpbT1jKDIsMykpCmluZGV4MkFycmF5CmFycjFbaW5kZXgyQXJyYXldCmEgPC0gYXJyYXkoMTo2LCBkaW0gPSBjKDIsMykpCmIgPC0gYXJyYXkoNzoxMiwgZGltID0gYygyLDMpKQphICogYgojIG91dGVyIHByb2R1Y3QKQSA8LSBhcnJheSgxOjE4LCBkaW0gPSBjKDMsMiwzKSkKQiA8LSBhcnJheSgxOTozNiwgZGltID0gYygyLDMsMykpCkEKQgpBQiA8LSBBICVvJSBCCmRpbShBQikKYGBgCgojIyBNYXRyaXplbgoKYGBge3J9CmFNYXRyaXggPC0gbWF0cml4KGMoMioxOjMsIDMqMTozKSwgbnJvdyA9IDIsIG5jb2wgPSAzKQphTWF0cml4CiMgVHJhbnNwb25pZXJlbgphbm90aGVyTWF0cml4IDwtIHQoYU1hdHJpeCkKIyBNYXRyaXplbm11bHRpcGxpa2F0aW9uCmFNYXRyaXggJSolIGFub3RoZXJNYXRyaXggCiMgS3JldXpwcm9kdWt0IHZvbiBBLCBCID09IHQoQSkgJSolIEIKY3Jvc3Nwcm9kKGFNYXRyaXgsMioxOjIpCmBgYAoKCiMjIEZha3RvcmVuCgpgYGB7cn0Kc3RhZHQgPC0gYygiQmVybGluIiwgIkRyZXNkZW4iLCAiSGFtYnVyZyIsICJCZXJsaW4iLCAiQmVybGluIiwgIkhhbWJ1cmciLCAiRHJlc2RlbiIpCmthdGVnb3JpZSA8LSBjKCJCZWtsZWlkdW5nIiwgIlNjaHVoZSIsICJLb3NtZXRpayIsICJLb3NtZXRpayIsICJTY2h1aGUiLCAiQmVrbGVpZHVuZyIsICJCZWtsZWlkdW5nIikKYmV0cmFnIDwtIGMoNTAwMCwgNDUwMCwgMzUwMCwgMjUwMCwgMTAwMCwgMjAwMCwgNTUwMCkKc3RhZHRBc0Zha3RvciA8LSBmYWN0b3Ioc3RhZHQpCnByaW50KHN0YWR0QXNGYWt0b3IpCmFzLm51bWVyaWMoc3RhZHRBc0Zha3RvcikKbGV2ZWxzKHN0YWR0QXNGYWt0b3IpCmxldmVscyhzdGFkdEFzRmFrdG9yKSA8LSBjKCJCRVIiLCAiRFJFIiwgIkhBTSIpCnN0YWR0Q29kZUZha3RvciA8LSBmYWN0b3Ioc3RhZHRBc0Zha3RvciwgbGFiZWxzPWMoIkIiLCAiRCIsICJIIikpCnByaW50KHN0YWR0Q29kZUZha3RvcikKdGFibGUoc3RhZHQpCnRhcHBseShiZXRyYWcsIGthdGVnb3JpZSwgc3VtKQpgYGAKCgoKCg==</div>

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

