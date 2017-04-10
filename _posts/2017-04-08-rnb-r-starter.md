---
permalink: /r-starter/
title: "R: Starter"
author_profile: true
layout: single-rnb
rnotebook: rnb-r-starter.Rmd
excerpt: "Es waren einmal Zahlen und die lebten in R. Ein kleiner Überblick über Typen, Zuweisung, Ausgabe, Operationen und Indizierung in R. Und ein Test für die Formatierung von R Notebooks - angelegt in RStudio - zur Darstellung mit Jekyll."
date: 2017-04-08 01:12:46 +02:00
last_modified_at: 2017-04-14 13:30:39 +02:00
tags: r howto notebook
---

<div class="fluid-row" id="header">

<aside class="sidebar__right">
<nav class="toc flyout-toc">
<header><h4 class="nav__title"><i class="fa fa-file-text"></i> TOC</h4></header>
<ul class="toc__menu toc_flyout" id="markdown-toc">
<li><a href="#r-lernen">R lernen</a></li>
<li><a href="#variablen-zuweisung-und-ausgabe">Variablen: Zuweisung und Ausgabe</a></li>
<li><a href="#datentypen">Datentypen</a></li>
<li><a href="#vektoren-zuweisung-arithmetik-und-indizierung">Vektoren: Zuweisung¸ Arithmetik und Indizierung</a></li>
<li><a href="#arrays">Arrays</a></li>
<li><a href="#matrizen">Matrizen</a></li>
<li><a href="#faktoren">Faktoren</a></li>
</ul>
</nav>
</aside>

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
<p>Ich bin bei <a href="https://depot.xda-developers.com/">XDA Developers</a>{:target=“_blank“} auf einige Online Kurse über Machine Learning gestoßen. Und da ich darüber schon immer mehr wissen wollte und neuer Kopf-Input gerade anstand, habe ich angefangen den Kurs zu schauen. Ich erinnerte mich außerdem, während des US Wahlkampfs diesen spannenden Artikel <a href="http://varianceexplained.org/r/trump-tweets/">Text analysis of Trump’s tweets confirms he writes only the (angrier) Android half</a>{:target=”_blank“} von <em>David Robinson von Stack Overflow</em> gelesen zu haben. Das wollte ich auch können. Also war es an der Zeit, das ganz alte Statistik-Wissen zu reanimieren und einzusteigen. Der Artikel ist nur eine Sammlung der ersten Tutorials über die Grundlagen von R – Variablen, Ein- und Ausgabe, Operationen. Eigenlich eher für mich als Wiederholung geschrieben. Und: Fast alles wird heute mit Torten und Balken begründet und wir <em>glauben</em>, sobald wir eine begründete Grafik sehen. Ich denke mal, da sollte man sie auch selbst herstellen können.</p>
</div>
<div id="variablen-zuweisung-und-ausgabe" class="section level2">
<h2>Variablen: Zuweisung und Ausgabe</h2>
<p>Die ersten Schritte im Umgang mit etwas Neuem sollten immer beginnen mit: Wie mache ich es an, wie mache ich es aus. Bei einer Programmmiersprache wäre das dann: Wie gebe ich etwas ein, wie gebe ich etwas aus. Und zum Ausgeben braucht man ein Ding genannt Variable. Daher fange ich damit an. Wie werden Variablen initialisiert, wie weise ich ihnen einen Wert zu und wie gebe ich sie dann aus. Als erstes die Initalisierung von Variablen und die Wertezuweisung mit =, -&gt; oder &lt;-. Und natürlich deren Ausgabe.</p>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZWluZVZhcmlhYmxlID0gMzJcbmFuZGVyZVZhcmlhYmxlIDwtIDI3XG4xOC43IC0+IGRyaXR0ZVZhcmlhYmxlXG5laW5lVmFyaWFibGVcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">eineVariable =<span class="st"> </span><span class="dv">32</span>
andereVariable &lt;-<span class="st"> </span><span class="dv">27</span>
<span class="fl">18.7</span> -&gt;<span class="st"> </span>dritteVariable
eineVariable</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDMyXG4ifQ== -->
<pre><code>[1] 32</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYW5kZXJlVmFyaWFibGVcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">andereVariable</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDI3XG4ifQ== -->
<pre><code>[1] 27</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZHJpdHRlVmFyaWFibGVcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">dritteVariable</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDE4LjdcbiJ9 -->
<pre><code>[1] 18.7</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZWluZVZhcmlhYmxlXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">eineVariable</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDMyXG4ifQ== -->
<pre><code>[1] 32</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZWluZVZhcmlhYmxlICsgYW5kZXJlVmFyaWFibGVcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">eineVariable +<span class="st"> </span>andereVariable</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDU5XG4ifQ== -->
<pre><code>[1] 59</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxucHJpbnQoZHJpdHRlVmFyaWFibGUpXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">print</span>(dritteVariable)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDE4LjdcbiJ9 -->
<pre><code>[1] 18.7</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZmlyc3RWYXIgPC0gc2Vjb25kVmFyIDwtIFwia29taXNjaFwiXG5jYXQoZmlyc3RWYXIsIFwiLFwiLCBzZWNvbmRWYXIsIFwiIC0gc2luZCBiZWlkZSBnbGVpY2ggLVwiLCBzZXAgPSBcIiBcIilcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">firstVar &lt;-<span class="st"> </span>secondVar &lt;-<span class="st"> &quot;komisch&quot;</span>
<span class="kw">cat</span>(firstVar, <span class="st">&quot;,&quot;</span>, secondVar, <span class="st">&quot; - sind beide gleich -&quot;</span>, <span class="dt">sep =</span> <span class="st">&quot; &quot;</span>)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoia29taXNjaCAsIGtvbWlzY2ggIC0gc2luZCBiZWlkZSBnbGVpY2ggLVxuIn0= -->
<pre><code>komisch , komisch  - sind beide gleich -</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYU1lc3NhZ2UgPSBwYXN0ZShmaXJzdFZhciwgXCItXCIsXCJkYXMgaXN0IGRhc3NlbGJlIHdpZVwiLCBzZWNvbmRWYXIsIHNlcCA9IFwiIFwiKVxubWVzc2FnZShhTWVzc2FnZSlcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">aMessage =<span class="st"> </span><span class="kw">paste</span>(firstVar, <span class="st">&quot;-&quot;</span>,<span class="st">&quot;das ist dasselbe wie&quot;</span>, secondVar, <span class="dt">sep =</span> <span class="st">&quot; &quot;</span>)
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
<p>Integer und Long, Character und String, Datum und Bool.</p>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaWNoQmluSW50ZWdlciA8LSA0TFxuaXMuaW50ZWdlcihpY2hCaW5JbnRlZ2VyKVxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">ichBinInteger &lt;-<span class="st"> </span>4L
<span class="kw">is.integer</span>(ichBinInteger)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFRSVUVcbiJ9 -->
<pre><code>[1] TRUE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaWNoQmluQXVjaEludGVnZXIgPC0gYXMuaW50ZWdlcigzKzUpXG5jbGFzcyhpY2hCaW5BdWNoSW50ZWdlcilcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">ichBinAuchInteger &lt;-<span class="st"> </span><span class="kw">as.integer</span>(<span class="dv">3+5</span>)
<span class="kw">class</span>(ichBinAuchInteger)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiaW50ZWdlclwiXG4ifQ== -->
<pre><code>[1] &quot;integer&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaXMubnVtZXJpYyhpY2hCaW5JbnRlZ2VyKVxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">is.numeric</span>(ichBinInteger)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFRSVUVcbiJ9 -->
<pre><code>[1] TRUE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaXMuaW50ZWdlcihpY2hCaW5BdWNoSW50ZWdlcilcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">is.integer</span>(ichBinAuchInteger)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFRSVUVcbiJ9 -->
<pre><code>[1] TRUE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaWNoQmluQnVjaHN0YWJlIDwtIFwiYW55IHN0cmluZ1wiXG5jbGFzcyhpY2hCaW5CdWNoc3RhYmUpXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">ichBinBuchstabe &lt;-<span class="st"> &quot;any string&quot;</span>
<span class="kw">class</span>(ichBinBuchstabe)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiY2hhcmFjdGVyXCJcbiJ9 -->
<pre><code>[1] &quot;character&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubmNoYXIoaWNoQmluQnVjaHN0YWJlKVxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">nchar</span>(ichBinBuchstabe)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDEwXG4ifQ== -->
<pre><code>[1] 10</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaWNoQmluRGF0dW0gPC0gYXMuRGF0ZShcIjIwMTYtMDItMTcgMDA6MjlcIilcbmljaEJpbkRhdHVtXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">ichBinDatum &lt;-<span class="st"> </span><span class="kw">as.Date</span>(<span class="st">&quot;2016-02-17 00:29&quot;</span>)
ichBinDatum</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiMjAxNi0wMi0xN1wiXG4ifQ== -->
<pre><code>[1] &quot;2016-02-17&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuY2xhc3MoaWNoQmluRGF0dW0pXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">class</span>(ichBinDatum)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiRGF0ZVwiXG4ifQ== -->
<pre><code>[1] &quot;Date&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXMubnVtZXJpYyhpY2hCaW5EYXR1bSlcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">as.numeric</span>(ichBinDatum)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDE2ODQ4XG4ifQ== -->
<pre><code>[1] 16848</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaWNoQmluQXVjaERhdHVtIDwtIGFzLkRhdGUoXCIyMDE2LTAyLTE0IDAwOjI5XCIpXG5pY2hCaW5EYXR1bS1pY2hCaW5BdWNoRGF0dW1cbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">ichBinAuchDatum &lt;-<span class="st"> </span><span class="kw">as.Date</span>(<span class="st">&quot;2016-02-14 00:29&quot;</span>)
ichBinDatum-ichBinAuchDatum</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiVGltZSBkaWZmZXJlbmNlIG9mIDMgZGF5c1xuIn0= -->
<pre><code>Time difference of 3 days</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuY2xhc3MoaWNoQmluRGF0dW0taWNoQmluQXVjaERhdHVtKVxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">class</span>(ichBinDatum-ichBinAuchDatum)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiZGlmZnRpbWVcIlxuIn0= -->
<pre><code>[1] &quot;difftime&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXMubnVtZXJpYyhpY2hCaW5EYXR1bS1pY2hCaW5BdWNoRGF0dW0pXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">as.numeric</span>(ichBinDatum-ichBinAuchDatum)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDNcbiJ9 -->
<pre><code>[1] 3</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaUFtVHJ1ZSA8LSBUUlVFXG5jbGFzcyhpQW1UcnVlKVxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">iAmTrue &lt;-<span class="st"> </span><span class="ot">TRUE</span>
<span class="kw">class</span>(iAmTrue)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwibG9naWNhbFwiXG4ifQ== -->
<pre><code>[1] &quot;logical&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaUFtTG9naWNhbCA8LSAyICE9IDNcbmlBbUxvZ2ljYWxcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">iAmLogical &lt;-<span class="st"> </span><span class="dv">2</span> !=<span class="st"> </span><span class="dv">3</span>
iAmLogical</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFRSVUVcbiJ9 -->
<pre><code>[1] TRUE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaUNvbXBhcmVDaGFyYWN0ZXJzIDwtIFwiUmVkXCIgPiBcIkJsdWVcIlxuaUNvbXBhcmVDaGFyYWN0ZXJzXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">iCompareCharacters &lt;-<span class="st"> &quot;Red&quot;</span> &gt;<span class="st"> &quot;Blue&quot;</span>
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
<p>Alles in R ist in gewisser Weise eine Liste, eine Reihe von Daten. Ein Vektor kann Elemente unterschiedlicher Datentypen beinhalten. Und ganz wichtig: Die Indizierung der Elemente beginnt bei 1.</p>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuc2ltcGxlU2VxdWVuY2UgPC0gMToxMlxuc2ltcGxlU2VxdWVuY2VcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">simpleSequence &lt;-<span class="st"> </span><span class="dv">1</span>:<span class="dv">12</span>
simpleSequence</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiIFsxXSAgMSAgMiAgMyAgNCAgNSAgNiAgNyAgOCAgOSAxMCAxMSAxMlxuIn0= -->
<pre><code> [1]  1  2  3  4  5  6  7  8  9 10 11 12</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZXZlbk51bWJlclNlcXVlbmNlIDwtIDIqMTo2XG5ldmVuTnVtYmVyU2VxdWVuY2VcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">evenNumberSequence &lt;-<span class="st"> </span><span class="dv">2</span>*<span class="dv">1</span>:<span class="dv">6</span>
evenNumberSequence</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAyICA0ICA2ICA4IDEwIDEyXG4ifQ== -->
<pre><code>[1]  2  4  6  8 10 12</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxucmVwZWF0U2VxdWVuY2UgPC0gcmVwKGV2ZW5OdW1iZXJTZXF1ZW5jZSwgdGltZXMgPSAyLCBsZW5ndGgub3V0ID0gMjAsIGVhY2ggPSAzKVxucmVwZWF0U2VxdWVuY2VcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">repeatSequence &lt;-<span class="st"> </span><span class="kw">rep</span>(evenNumberSequence, <span class="dt">times =</span> <span class="dv">2</span>, <span class="dt">length.out =</span> <span class="dv">20</span>, <span class="dt">each =</span> <span class="dv">3</span>)
repeatSequence</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiIFsxXSAgMiAgMiAgMiAgNCAgNCAgNCAgNiAgNiAgNiAgOCAgOCAgOCAxMCAxMCAxMCAxMiAxMiAxMiAgMiAgMlxuIn0= -->
<pre><code> [1]  2  2  2  4  4  4  6  6  6  8  8  8 10 10 10 12 12 12  2  2</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZ2VuZXJhbFNlcXVlbmNlIDwtIHNlcShmcm9tID0gLTUsIHRvID0gMTAsIGJ5ID0gMC4yKVxuZ2VuZXJhbFNlcXVlbmNlXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">generalSequence &lt;-<span class="st"> </span><span class="kw">seq</span>(<span class="dt">from =</span> -<span class="dv">5</span>, <span class="dt">to =</span> <span class="dv">10</span>, <span class="dt">by =</span> <span class="fl">0.2</span>)
generalSequence</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiIFsxXSAtNS4wIC00LjggLTQuNiAtNC40IC00LjIgLTQuMCAtMy44IC0zLjYgLTMuNCAtMy4yIC0zLjAgLTIuOCAtMi42IC0yLjQgLTIuMiAtMi4wIC0xLjggLTEuNiAtMS40IC0xLjIgLTEuMCAtMC44IC0wLjYgLTAuNCAtMC4yXG5bMjZdICAwLjAgIDAuMiAgMC40ICAwLjYgIDAuOCAgMS4wICAxLjIgIDEuNCAgMS42ICAxLjggIDIuMCAgMi4yICAyLjQgIDIuNiAgMi44ICAzLjAgIDMuMiAgMy40ICAzLjYgIDMuOCAgNC4wICA0LjIgIDQuNCAgNC42ICA0Ljhcbls1MV0gIDUuMCAgNS4yICA1LjQgIDUuNiAgNS44ICA2LjAgIDYuMiAgNi40ICA2LjYgIDYuOCAgNy4wICA3LjIgIDcuNCAgNy42ICA3LjggIDguMCAgOC4yICA4LjQgIDguNiAgOC44ICA5LjAgIDkuMiAgOS40ICA5LjYgIDkuOFxuWzc2XSAxMC4wXG4ifQ== -->
<pre><code> [1] -5.0 -4.8 -4.6 -4.4 -4.2 -4.0 -3.8 -3.6 -3.4 -3.2 -3.0 -2.8 -2.6 -2.4 -2.2 -2.0 -1.8 -1.6 -1.4 -1.2 -1.0 -0.8 -0.6 -0.4 -0.2
[26]  0.0  0.2  0.4  0.6  0.8  1.0  1.2  1.4  1.6  1.8  2.0  2.2  2.4  2.6  2.8  3.0  3.2  3.4  3.6  3.8  4.0  4.2  4.4  4.6  4.8
[51]  5.0  5.2  5.4  5.6  5.8  6.0  6.2  6.4  6.6  6.8  7.0  7.2  7.4  7.6  7.8  8.0  8.2  8.4  8.6  8.8  9.0  9.2  9.4  9.6  9.8
[76] 10.0</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjMSA8LSBjKDI0NywgMzUwLCBcIlRlc3RcIiwgVFJVRSwgNjAwKVxubW9kZSh2ZWMxKVxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">vec1 &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="dv">247</span>, <span class="dv">350</span>, <span class="st">&quot;Test&quot;</span>, <span class="ot">TRUE</span>, <span class="dv">600</span>)
<span class="kw">mode</span>(vec1)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiY2hhcmFjdGVyXCJcbiJ9 -->
<pre><code>[1] &quot;character&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudHlwZW9mKHZlYzEpXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">typeof</span>(vec1)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiY2hhcmFjdGVyXCJcbiJ9 -->
<pre><code>[1] &quot;character&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjMiA8LSBudW1lcmljKDUpXG52ZWMyXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">vec2 &lt;-<span class="st"> </span><span class="kw">numeric</span>(<span class="dv">5</span>)
vec2</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDAgMCAwIDAgMFxuIn0= -->
<pre><code>[1] 0 0 0 0 0</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjMyA8LSBjKHZlYzIsIHZlYzEpXG52ZWMzXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">vec3 &lt;-<span class="st"> </span><span class="kw">c</span>(vec2, vec1)
vec3</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiIFsxXSBcIjBcIiAgICBcIjBcIiAgICBcIjBcIiAgICBcIjBcIiAgICBcIjBcIiAgICBcIjI0N1wiICBcIjM1MFwiICBcIlRlc3RcIiBcIlRSVUVcIiBcIjYwMFwiIFxuIn0= -->
<pre><code> [1] &quot;0&quot;    &quot;0&quot;    &quot;0&quot;    &quot;0&quot;    &quot;0&quot;    &quot;247&quot;  &quot;350&quot;  &quot;Test&quot; &quot;TRUE&quot; &quot;600&quot; </code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjMTAgPC0gYygxLCA1LCAxMCwgMjAsIDUwLCAxMDAsIDUwMClcbnZlYzIwIDwtIGMoMCwgMzApXG5mb3IoaSBpbiB2ZWMxMCkge1xuICB2ZWMyMCA8LSBjKHZlYzIwICwgaSozMClcbn1cbnZlYzIwXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">vec10 &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="dv">1</span>, <span class="dv">5</span>, <span class="dv">10</span>, <span class="dv">20</span>, <span class="dv">50</span>, <span class="dv">100</span>, <span class="dv">500</span>)
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
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">vec30 &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="dv">5</span>, <span class="dv">5</span>, <span class="dv">5</span>, <span class="dv">6</span>, <span class="dv">2</span>, <span class="dv">2</span>, <span class="dv">2</span>)
vec40 &lt;-<span class="st"> </span>vec30 *<span class="st"> </span>vec10
vec40</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAgIDUgICAyNSAgIDUwICAxMjAgIDEwMCAgMjAwIDEwMDBcbiJ9 -->
<pre><code>[1]    5   25   50  120  100  200 1000</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjNTAgPC0gdmVjNDAgKyBjKDEwMCwwKVxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">vec50 &lt;-<span class="st"> </span>vec40 +<span class="st"> </span><span class="kw">c</span>(<span class="dv">100</span>,<span class="dv">0</span>)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiTMOkbmdlIGRlcyBsw6RuZ2VyZW4gT2JqZWt0ZXNcbiBcdCBpc3Qga2VpbiBWaWVsZmFjaGVzIGRlciBMw6RuZ2UgZGVzIGvDvHJ6ZXJlbiBPYmpla3Rlc1xuIn0= -->
<pre><code>Länge des längeren Objektes
     ist kein Vielfaches der Länge des kürzeren Objektes</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudmVjNTBcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">vec50</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAxMDUgICAyNSAgMTUwICAxMjAgIDIwMCAgMjAwIDExMDBcbiJ9 -->
<pre><code>[1]  105   25  150  120  200  200 1100</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuc2VxMSA8LSAxOjRcbnNlcTEgPT0gMlxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">seq1 &lt;-<span class="st"> </span><span class="dv">1</span>:<span class="dv">4</span>
seq1 ==<span class="st"> </span><span class="dv">2</span></code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIEZBTFNFICBUUlVFIEZBTFNFIEZBTFNFXG4ifQ== -->
<pre><code>[1] FALSE  TRUE FALSE FALSE</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuc3RyaW5nU2VxIDwtIGMoXCJBXCIsIFwiQlwiLCBcIkNcIiwgXCJEXCIsIFwiRVwiLCBcIkZcIiwgXCJHXCIsIFwiSFwiKVxuZnVua3lTZXEgPC0gcGFzdGUoc3RyaW5nU2VxLCBzZXExLCBzZXA9XCJcIilcbmZ1bmt5U2VxXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">stringSeq &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;A&quot;</span>, <span class="st">&quot;B&quot;</span>, <span class="st">&quot;C&quot;</span>, <span class="st">&quot;D&quot;</span>, <span class="st">&quot;E&quot;</span>, <span class="st">&quot;F&quot;</span>, <span class="st">&quot;G&quot;</span>, <span class="st">&quot;H&quot;</span>)
funkySeq &lt;-<span class="st"> </span><span class="kw">paste</span>(stringSeq, seq1, <span class="dt">sep=</span><span class="st">&quot;&quot;</span>)
funkySeq</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiQTFcIiBcIkIyXCIgXCJDM1wiIFwiRDRcIiBcIkUxXCIgXCJGMlwiIFwiRzNcIiBcIkg0XCJcbiJ9 -->
<pre><code>[1] &quot;A1&quot; &quot;B2&quot; &quot;C3&quot; &quot;D4&quot; &quot;E1&quot; &quot;F2&quot; &quot;G3&quot; &quot;H4&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubWVpbmVTZXEgPC0gMyoxOjVcbm1laW5lU2VxW3JlcChjKDEsMyksIHRpbWVzID0gNSldXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">meineSeq &lt;-<span class="st"> </span><span class="dv">3</span>*<span class="dv">1</span>:<span class="dv">5</span>
meineSeq[<span class="kw">rep</span>(<span class="kw">c</span>(<span class="dv">1</span>,<span class="dv">3</span>), <span class="dt">times =</span> <span class="dv">5</span>)]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiIFsxXSAzIDkgMyA5IDMgOSAzIDkgMyA5XG4ifQ== -->
<pre><code> [1] 3 9 3 9 3 9 3 9 3 9</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubWVpbmVTZXFbYygtMywgLTQpXVxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">meineSeq[<span class="kw">c</span>(-<span class="dv">3</span>, -<span class="dv">4</span>)]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAzICA2IDE1XG4ifQ== -->
<pre><code>[1]  3  6 15</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubmFtZXMobWVpbmVTZXEpIDwtIGMoXCJBXCIsXCJCXCIsXCJDXCIsXCJEXCIsXCJFXCIpXG5tZWluZVNlcVtjKFwiQVwiLFwiQ1wiKV1cbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">names</span>(meineSeq) &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;A&quot;</span>,<span class="st">&quot;B&quot;</span>,<span class="st">&quot;C&quot;</span>,<span class="st">&quot;D&quot;</span>,<span class="st">&quot;E&quot;</span>)
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
<p>Ein Array ist eine Vektor, dessen Werte in den Dimensionen des Arrays angeordnet sind. Das kann man sich so vorstellen, das z.B. bei einem 2-dimensionalen Array dieses mit den Werten des Vektors beginnend bei dem Element <em>links oben</em> zuerst die Zeilen (row) nach unten gefüllt werden und dann in die nächste Spalte (col) nach oben gesprungen wird und diese zeilenweise aufgefüllt wird.</p>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMSA8LSBhcnJheShjKDE6MTIpLCBkaW0gPSBjKDMsMiwyKSlcbmFycjFcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">arr1 &lt;-<span class="st"> </span><span class="kw">array</span>(<span class="kw">c</span>(<span class="dv">1</span>:<span class="dv">12</span>), <span class="dt">dim =</span> <span class="kw">c</span>(<span class="dv">3</span>,<span class="dv">2</span>,<span class="dv">2</span>))
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
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">arr2 &lt;-<span class="st"> </span><span class="kw">array</span>(<span class="kw">c</span>(<span class="dv">1</span>,<span class="dv">0</span>) , <span class="dt">dim =</span> <span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>))
arr2</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgICAxICAgIDEgICAgMVxuWzIsXSAgICAwICAgIDAgICAgMFxuIn0= -->
<pre><code>     [,1] [,2] [,3]
[1,]    1    1    1
[2,]    0    0    0</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMVsyLDIsMV1cbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">arr1[<span class="dv">2</span>,<span class="dv">2</span>,<span class="dv">1</span>]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDVcbiJ9 -->
<pre><code>[1] 5</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMVsyOjMsLDFdXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">arr1[<span class="dv">2</span>:<span class="dv">3</span>,,<span class="dv">1</span>]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl1cblsxLF0gICAgMiAgICA1XG5bMixdICAgIDMgICAgNlxuIn0= -->
<pre><code>     [,1] [,2]
[1,]    2    5
[2,]    3    6</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaW5kZXhBcnJheSA8LSBhcnJheSAoYygxOjIpLCBkaW09YygyLDMpKVxuaW5kZXhBcnJheVxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">indexArray &lt;-<span class="st"> </span><span class="kw">array</span> (<span class="kw">c</span>(<span class="dv">1</span>:<span class="dv">2</span>), <span class="dt">dim=</span><span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>))
indexArray</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgICAxICAgIDEgICAgMVxuWzIsXSAgICAyICAgIDIgICAgMlxuIn0= -->
<pre><code>     [,1] [,2] [,3]
[1,]    1    1    1
[2,]    2    2    2</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMVtpbmRleEFycmF5XVxuYGBgIn0= -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">arr1[indexArray]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdICAxIDExXG4ifQ== -->
<pre><code>[1]  1 11</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaW5kZXgyQXJyYXkgPC0gYXJyYXkgKGMoMiwzLDIsMSwxLDIpLCBkaW09YygyLDMpKVxuaW5kZXgyQXJyYXlcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">index2Array &lt;-<span class="st"> </span><span class="kw">array</span> (<span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>,<span class="dv">2</span>,<span class="dv">1</span>,<span class="dv">1</span>,<span class="dv">2</span>), <span class="dt">dim=</span><span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>))
index2Array</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgICAyICAgIDIgICAgMVxuWzIsXSAgICAzICAgIDEgICAgMlxuIn0= -->
<pre><code>     [,1] [,2] [,3]
[1,]    2    2    1
[2,]    3    1    2</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYXJyMVtpbmRleDJBcnJheV1cbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">arr1[index2Array]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDUgOVxuIn0= -->
<pre><code>[1] 5 9</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYSA8LSBhcnJheSgxOjYsIGRpbSA9IGMoMiwzKSlcbmIgPC0gYXJyYXkoNzoxMiwgZGltID0gYygyLDMpKVxuYSAqIGJcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">a &lt;-<span class="st"> </span><span class="kw">array</span>(<span class="dv">1</span>:<span class="dv">6</span>, <span class="dt">dim =</span> <span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>))
b &lt;-<span class="st"> </span><span class="kw">array</span>(<span class="dv">7</span>:<span class="dv">12</span>, <span class="dt">dim =</span> <span class="kw">c</span>(<span class="dv">2</span>,<span class="dv">3</span>))
a *<span class="st"> </span>b</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgICA3ICAgMjcgICA1NVxuWzIsXSAgIDE2ICAgNDAgICA3MlxuIn0= -->
<pre><code>     [,1] [,2] [,3]
[1,]    7   27   55
[2,]   16   40   72</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuIyBvdXRlciBwcm9kdWN0XG5BIDwtIGFycmF5KDE6MTgsIGRpbSA9IGMoMywyLDMpKVxuQiA8LSBhcnJheSgxOTozNiwgZGltID0gYygyLDMsMykpXG5BXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="co"># outer product</span>
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
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">B</code></pre></div>
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
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">AB &lt;-<span class="st"> </span>A %o%<span class="st"> </span>B
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
<p>Matrizen sind 2-dimensionale Arrays mit besonderen Möglichkeiten. Lineare Gleichungen lassen sich z.B. mit Matrizenarithmetik lösen.</p>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuYU1hdHJpeCA8LSBtYXRyaXgoYygyKjE6MywgMyoxOjMpLCBucm93ID0gMiwgbmNvbCA9IDMpXG5hTWF0cml4XG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">aMatrix &lt;-<span class="st"> </span><span class="kw">matrix</span>(<span class="kw">c</span>(<span class="dv">2</span>*<span class="dv">1</span>:<span class="dv">3</span>, <span class="dv">3</span>*<span class="dv">1</span>:<span class="dv">3</span>), <span class="dt">nrow =</span> <span class="dv">2</span>, <span class="dt">ncol =</span> <span class="dv">3</span>)
aMatrix</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiICAgICBbLDFdIFssMl0gWywzXVxuWzEsXSAgICAyICAgIDYgICAgNlxuWzIsXSAgICA0ICAgIDMgICAgOVxuIn0= -->
<pre><code>     [,1] [,2] [,3]
[1,]    2    6    6
[2,]    4    3    9</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuIyBUcmFuc3BvbmllcmVuXG5hbm90aGVyTWF0cml4IDwtIHQoYU1hdHJpeClcbiMgTWF0cml6ZW5tdWx0aXBsaWthdGlvblxuYU1hdHJpeCAlKiUgYW5vdGhlck1hdHJpeCBcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="co"># Transponieren</span>
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
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="co"># Kreuzprodukt von A, B == t(A) %*% B</span>
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
<p>Ein Vektor kann in Faktoren, den Gruppen gleicher Werte, zerlegt werden. Das ist vergleichbar einem <code>GROUP BY</code> in SQL.</p>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuc3RhZHQgPC0gYyhcIkJlcmxpblwiLCBcIkRyZXNkZW5cIiwgXCJIYW1idXJnXCIsIFwiQmVybGluXCIsIFwiQmVybGluXCIsIFwiSGFtYnVyZ1wiLCBcIkRyZXNkZW5cIilcbmthdGVnb3JpZSA8LSBjKFwiQmVrbGVpZHVuZ1wiLCBcIlNjaHVoZVwiLCBcIktvc21ldGlrXCIsIFwiS29zbWV0aWtcIiwgXCJTY2h1aGVcIiwgXCJCZWtsZWlkdW5nXCIsIFwiQmVrbGVpZHVuZ1wiKVxuYmV0cmFnIDwtIGMoNTAwMCwgNDUwMCwgMzUwMCwgMjUwMCwgMTAwMCwgMjAwMCwgNTUwMClcbnN0YWR0QXNGYWt0b3IgPC0gZmFjdG9yKHN0YWR0KVxucHJpbnQoc3RhZHRBc0Zha3RvcilcbmBgYCJ9 -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">stadt &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;Berlin&quot;</span>, <span class="st">&quot;Dresden&quot;</span>, <span class="st">&quot;Hamburg&quot;</span>, <span class="st">&quot;Berlin&quot;</span>, <span class="st">&quot;Berlin&quot;</span>, <span class="st">&quot;Hamburg&quot;</span>, <span class="st">&quot;Dresden&quot;</span>)
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
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">as.numeric</span>(stadtAsFaktor)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDEgMiAzIDEgMSAzIDJcbiJ9 -->
<pre><code>[1] 1 2 3 1 1 3 2</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubGV2ZWxzKHN0YWR0QXNGYWt0b3IpXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">levels</span>(stadtAsFaktor)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiQmVybGluXCIgIFwiRHJlc2RlblwiIFwiSGFtYnVyZ1wiXG4ifQ== -->
<pre><code>[1] &quot;Berlin&quot;  &quot;Dresden&quot; &quot;Hamburg&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubGV2ZWxzKHN0YWR0QXNGYWt0b3IpIDwtIGMoXCJCRVJcIiwgXCJEUkVcIiwgXCJIQU1cIilcbnN0YWR0Q29kZUZha3RvciA8LSBmYWN0b3Ioc3RhZHRBc0Zha3RvciwgbGFiZWxzPWMoXCJCXCIsIFwiRFwiLCBcIkhcIikpXG5wcmludChzdGFkdENvZGVGYWt0b3IpXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">levels</span>(stadtAsFaktor) &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;BER&quot;</span>, <span class="st">&quot;DRE&quot;</span>, <span class="st">&quot;HAM&quot;</span>)
stadtCodeFaktor &lt;-<span class="st"> </span><span class="kw">factor</span>(stadtAsFaktor, <span class="dt">labels=</span><span class="kw">c</span>(<span class="st">&quot;B&quot;</span>, <span class="st">&quot;D&quot;</span>, <span class="st">&quot;H&quot;</span>))
<span class="kw">print</span>(stadtCodeFaktor)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIEIgRCBIIEIgQiBIIERcbkxldmVsczogQiBEIEhcbiJ9 -->
<pre><code>[1] B D H B B H D
Levels: B D H</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudGFibGUoc3RhZHQpXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">table</span>(stadt)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoic3RhZHRcbiBCZXJsaW4gRHJlc2RlbiBIYW1idXJnIFxuICAgICAgMyAgICAgICAyICAgICAgIDIgXG4ifQ== -->
<pre><code>stadt
 Berlin Dresden Hamburg 
      3       2       2 </code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxudGFwcGx5KGJldHJhZywga2F0ZWdvcmllLCBzdW0pXG5gYGAifQ== -->
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r"><span class="kw">tapply</span>(betrag, kategorie, sum)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiQmVrbGVpZHVuZyAgIEtvc21ldGlrICAgICBTY2h1aGUgXG4gICAgIDEyNTAwICAgICAgIDYwMDAgICAgICAgNTUwMCBcbiJ9 -->
<pre><code>Bekleidung   Kosmetik     Schuhe 
     12500       6000       5500 </code></pre>
<!-- rnb-output-end -->
<!-- rnb-chunk-end -->
<!-- rnb-text-begin -->
<!-- rnb-text-end -->
</div>

<div id="rmd-source-code">LS0tCnRpdGxlOiAiUiBTdGFydGVyIgpvdXRwdXQ6CiAgaHRtbF9ub3RlYm9vazoKICAgIGNvZGVfZm9sZGluZzogbm9uZQogICAgZGZfcHJpbnQ6IGthYmxlCiAgICBoaWdobGlnaHQ6IHB5Z21lbnRzCiAgICB0aGVtZTogZmxhdGx5CiAgICB0b2M6IHllcwogIGh0bWxfZG9jdW1lbnQ6CiAgICBoaWdobGlnaHQ6IHB5Z21lbnRzCiAgICBrZWVwX21kOiB5ZXMKLS0tCgojIyBSIGxlcm5lbgoKSWNoIGJpbiBiZWkgW1hEQSBEZXZlbG9wZXJzXShodHRwczovL2RlcG90LnhkYS1kZXZlbG9wZXJzLmNvbS8pezp0YXJnZXQ9Il9ibGFuayJ9IGF1ZiBlaW5pZ2UgT25saW5lIEt1cnNlIMO8YmVyIE1hY2hpbmUgTGVhcm5pbmcgZ2VzdG/Dn2VuLiBVbmQgZGEgaWNoIGRhcsO8YmVyIHNjaG9uIGltbWVyIG1laHIgd2lzc2VuIHdvbGx0ZSB1bmQgbmV1ZXIgS29wZi1JbnB1dCBnZXJhZGUgYW5zdGFuZCwgaGFiZSBpY2ggYW5nZWZhbmdlbiBkZW4gS3VycyB6dSBzY2hhdWVuLiBJY2ggZXJpbm5lcnRlIG1pY2ggYXXDn2VyZGVtLCB3w6RocmVuZCBkZXMgVVMgV2FobGthbXBmcyBkaWVzZW4gc3Bhbm5lbmRlbiBBcnRpa2VsIFtUZXh0IGFuYWx5c2lzIG9mIFRydW1wJ3MgdHdlZXRzIGNvbmZpcm1zIGhlIHdyaXRlcyBvbmx5IHRoZSAoYW5ncmllcikgQW5kcm9pZCBoYWxmXShodHRwOi8vdmFyaWFuY2VleHBsYWluZWQub3JnL3IvdHJ1bXAtdHdlZXRzLyl7OnRhcmdldD0iX2JsYW5rIn0gdm9uIF9EYXZpZCBSb2JpbnNvbiB2b24gU3RhY2sgT3ZlcmZsb3dfIGdlbGVzZW4genUgaGFiZW4uIERhcyB3b2xsdGUgaWNoIGF1Y2gga8O2bm5lbi4gQWxzbyB3YXIgZXMgYW4gZGVyIFplaXQsIGRhcyBnYW56IGFsdGUgU3RhdGlzdGlrLVdpc3NlbiB6dSByZWFuaW1pZXJlbiB1bmQgZWluenVzdGVpZ2VuLiBEZXIgQXJ0aWtlbCBpc3QgbnVyIGVpbmUgU2FtbWx1bmcgZGVyIGVyc3RlbiBUdXRvcmlhbHMgw7xiZXIgZGllIEdydW5kbGFnZW4gdm9uIFIgLS0gVmFyaWFibGVuLCBFaW4tIHVuZCBBdXNnYWJlLCBPcGVyYXRpb25lbi4gRWlnZW5saWNoIGVoZXIgZsO8ciBtaWNoIGFscyBXaWVkZXJob2x1bmcgZ2VzY2hyaWViZW4uIFVuZDogRmFzdCBhbGxlcyB3aXJkIGhldXRlIG1pdCBUb3J0ZW4gdW5kIEJhbGtlbiBiZWdyw7xuZGV0IHVuZCB3aXIgX2dsYXViZW5fLCBzb2JhbGQgd2lyIGVpbmUgYmVncsO8bmRldGUgR3JhZmlrIHNlaGVuLiBJY2ggZGVua2UgbWFsLCBkYSBzb2xsdGUgbWFuIHNpZSBhdWNoIHNlbGJzdCBoZXJzdGVsbGVuIGvDtm5uZW4uCgojIyBWYXJpYWJsZW46IFp1d2Vpc3VuZyB1bmQgQXVzZ2FiZQoKRGllIGVyc3RlbiBTY2hyaXR0ZSBpbSBVbWdhbmcgbWl0IGV0d2FzIE5ldWVtIHNvbGx0ZW4gaW1tZXIgYmVnaW5uZW4gbWl0OiBXaWUgbWFjaGUgaWNoIGVzIGFuLCB3aWUgbWFjaGUgaWNoIGVzIGF1cy4gQmVpIGVpbmVyIFByb2dyYW1tbWllcnNwcmFjaGUgd8OkcmUgZGFzIGRhbm46IFdpZSBnZWJlIGljaCBldHdhcyBlaW4sIHdpZSBnZWJlIGljaCBldHdhcyBhdXMuIFVuZCB6dW0gQXVzZ2ViZW4gYnJhdWNodCBtYW4gZWluIERpbmcgZ2VuYW5udCBWYXJpYWJsZS4gRGFoZXIgZmFuZ2UgaWNoIGRhbWl0IGFuLiBXaWUgd2VyZGVuIFZhcmlhYmxlbiBpbml0aWFsaXNpZXJ0LCB3aWUgd2Vpc2UgaWNoIGlobmVuIGVpbmVuIFdlcnQgenUgdW5kIHdpZSBnZWJlIGljaCBzaWUgZGFubiBhdXMuCkFscyBlcnN0ZXMgZGllIEluaXRhbGlzaWVydW5nIHZvbiBWYXJpYWJsZW4gdW5kIGRpZSBXZXJ0ZXp1d2Vpc3VuZyBtaXQgPSwgLT4gb2RlciA8LS4gVW5kIG5hdMO8cmxpY2ggZGVyZW4gQXVzZ2FiZS4KCmBgYHtyfQplaW5lVmFyaWFibGUgPSAzMgphbmRlcmVWYXJpYWJsZSA8LSAyNwoxOC43IC0+IGRyaXR0ZVZhcmlhYmxlCmVpbmVWYXJpYWJsZQphbmRlcmVWYXJpYWJsZQpkcml0dGVWYXJpYWJsZQplaW5lVmFyaWFibGUKZWluZVZhcmlhYmxlICsgYW5kZXJlVmFyaWFibGUKcHJpbnQoZHJpdHRlVmFyaWFibGUpCmZpcnN0VmFyIDwtIHNlY29uZFZhciA8LSAia29taXNjaCIKY2F0KGZpcnN0VmFyLCAiLCIsIHNlY29uZFZhciwgIiAtIHNpbmQgYmVpZGUgZ2xlaWNoIC0iLCBzZXAgPSAiICIpCmFNZXNzYWdlID0gcGFzdGUoZmlyc3RWYXIsICItIiwiZGFzIGlzdCBkYXNzZWxiZSB3aWUiLCBzZWNvbmRWYXIsIHNlcCA9ICIgIikKbWVzc2FnZShhTWVzc2FnZSkKYGBgCgojIyBEYXRlbnR5cGVuCgpJbnRlZ2VyIHVuZCBMb25nLCBDaGFyYWN0ZXIgdW5kIFN0cmluZywgRGF0dW0gdW5kIEJvb2wuIAoKYGBge3J9CmljaEJpbkludGVnZXIgPC0gNEwKaXMuaW50ZWdlcihpY2hCaW5JbnRlZ2VyKQppY2hCaW5BdWNoSW50ZWdlciA8LSBhcy5pbnRlZ2VyKDMrNSkKY2xhc3MoaWNoQmluQXVjaEludGVnZXIpCmlzLm51bWVyaWMoaWNoQmluSW50ZWdlcikKaXMuaW50ZWdlcihpY2hCaW5BdWNoSW50ZWdlcikKaWNoQmluQnVjaHN0YWJlIDwtICJhbnkgc3RyaW5nIgpjbGFzcyhpY2hCaW5CdWNoc3RhYmUpCm5jaGFyKGljaEJpbkJ1Y2hzdGFiZSkKaWNoQmluRGF0dW0gPC0gYXMuRGF0ZSgiMjAxNi0wMi0xNyAwMDoyOSIpCmljaEJpbkRhdHVtCmNsYXNzKGljaEJpbkRhdHVtKQphcy5udW1lcmljKGljaEJpbkRhdHVtKQppY2hCaW5BdWNoRGF0dW0gPC0gYXMuRGF0ZSgiMjAxNi0wMi0xNCAwMDoyOSIpCmljaEJpbkRhdHVtLWljaEJpbkF1Y2hEYXR1bQpjbGFzcyhpY2hCaW5EYXR1bS1pY2hCaW5BdWNoRGF0dW0pCmFzLm51bWVyaWMoaWNoQmluRGF0dW0taWNoQmluQXVjaERhdHVtKQppQW1UcnVlIDwtIFRSVUUKY2xhc3MoaUFtVHJ1ZSkKaUFtTG9naWNhbCA8LSAyICE9IDMKaUFtTG9naWNhbAppQ29tcGFyZUNoYXJhY3RlcnMgPC0gIlJlZCIgPiAiQmx1ZSIKaUNvbXBhcmVDaGFyYWN0ZXJzCmBgYAoKIyMgVmVrdG9yZW46IFp1d2Vpc3VuZ8K4IEFyaXRobWV0aWsgdW5kIEluZGl6aWVydW5nCgpBbGxlcyBpbiBSIGlzdCBpbiBnZXdpc3NlciBXZWlzZSBlaW5lIExpc3RlLCBlaW5lIFJlaWhlIHZvbiBEYXRlbi4gRWluIFZla3RvciBrYW5uIEVsZW1lbnRlIHVudGVyc2NoaWVkbGljaGVyIERhdGVudHlwZW4gYmVpbmhhbHRlbi4gVW5kIGdhbnogd2ljaHRpZzogRGllIEluZGl6aWVydW5nIGRlciBFbGVtZW50ZSBiZWdpbm50IGJlaSAxLiAKCmBgYHtyfQpzaW1wbGVTZXF1ZW5jZSA8LSAxOjEyCnNpbXBsZVNlcXVlbmNlCmV2ZW5OdW1iZXJTZXF1ZW5jZSA8LSAyKjE6NgpldmVuTnVtYmVyU2VxdWVuY2UKcmVwZWF0U2VxdWVuY2UgPC0gcmVwKGV2ZW5OdW1iZXJTZXF1ZW5jZSwgdGltZXMgPSAyLCBsZW5ndGgub3V0ID0gMjAsIGVhY2ggPSAzKQpyZXBlYXRTZXF1ZW5jZQpnZW5lcmFsU2VxdWVuY2UgPC0gc2VxKGZyb20gPSAtNSwgdG8gPSAxMCwgYnkgPSAwLjIpCmdlbmVyYWxTZXF1ZW5jZQp2ZWMxIDwtIGMoMjQ3LCAzNTAsICJUZXN0IiwgVFJVRSwgNjAwKQptb2RlKHZlYzEpCnR5cGVvZih2ZWMxKQp2ZWMyIDwtIG51bWVyaWMoNSkKdmVjMgp2ZWMzIDwtIGModmVjMiwgdmVjMSkKdmVjMwp2ZWMxMCA8LSBjKDEsIDUsIDEwLCAyMCwgNTAsIDEwMCwgNTAwKQp2ZWMyMCA8LSBjKDAsIDMwKQpmb3IoaSBpbiB2ZWMxMCkgewogIHZlYzIwIDwtIGModmVjMjAgLCBpKjMwKQp9CnZlYzIwCnZlYzMwIDwtIGMoNSwgNSwgNSwgNiwgMiwgMiwgMikKdmVjNDAgPC0gdmVjMzAgKiB2ZWMxMAp2ZWM0MAp2ZWM1MCA8LSB2ZWM0MCArIGMoMTAwLDApCnZlYzUwCnNlcTEgPC0gMTo0CnNlcTEgPT0gMgpzdHJpbmdTZXEgPC0gYygiQSIsICJCIiwgIkMiLCAiRCIsICJFIiwgIkYiLCAiRyIsICJIIikKZnVua3lTZXEgPC0gcGFzdGUoc3RyaW5nU2VxLCBzZXExLCBzZXA9IiIpCmZ1bmt5U2VxCm1laW5lU2VxIDwtIDMqMTo1Cm1laW5lU2VxW3JlcChjKDEsMyksIHRpbWVzID0gNSldCm1laW5lU2VxW2MoLTMsIC00KV0KbmFtZXMobWVpbmVTZXEpIDwtIGMoIkEiLCJCIiwiQyIsIkQiLCJFIikKbWVpbmVTZXFbYygiQSIsIkMiKV0KYGBgCgojIyBBcnJheXMKCkVpbiBBcnJheSBpc3QgZWluZSBWZWt0b3IsIGRlc3NlbiBXZXJ0ZSBpbiBkZW4gRGltZW5zaW9uZW4gZGVzIEFycmF5cyBhbmdlb3JkbmV0IHNpbmQuIERhcyBrYW5uIG1hbiBzaWNoIHNvIHZvcnN0ZWxsZW4sIGRhcyB6LkIuIGJlaSBlaW5lbSAyLWRpbWVuc2lvbmFsZW4gQXJyYXkgZGllc2VzIG1pdCBkZW4gV2VydGVuIGRlcyBWZWt0b3JzIGJlZ2lubmVuZCBiZWkgZGVtIEVsZW1lbnQgX2xpbmtzIG9iZW5fIHp1ZXJzdCBkaWUgWmVpbGVuIChyb3cpIG5hY2ggdW50ZW4gZ2Vmw7xsbHQgd2VyZGVuIHVuZCBkYW5uIGluIGRpZSBuw6RjaHN0ZSBTcGFsdGUgKGNvbCkgbmFjaCBvYmVuIGdlc3BydW5nZW4gd2lyZCB1bmQgZGllc2UgemVpbGVud2Vpc2UgYXVmZ2Vmw7xsbHQgd2lyZC4gCgpgYGB7cn0KYXJyMSA8LSBhcnJheShjKDE6MTIpLCBkaW0gPSBjKDMsMiwyKSkKYXJyMQphcnIyIDwtIGFycmF5KGMoMSwwKSAsIGRpbSA9IGMoMiwzKSkKYXJyMgphcnIxWzIsMiwxXQphcnIxWzI6MywsMV0KaW5kZXhBcnJheSA8LSBhcnJheSAoYygxOjIpLCBkaW09YygyLDMpKQppbmRleEFycmF5CmFycjFbaW5kZXhBcnJheV0KaW5kZXgyQXJyYXkgPC0gYXJyYXkgKGMoMiwzLDIsMSwxLDIpLCBkaW09YygyLDMpKQppbmRleDJBcnJheQphcnIxW2luZGV4MkFycmF5XQphIDwtIGFycmF5KDE6NiwgZGltID0gYygyLDMpKQpiIDwtIGFycmF5KDc6MTIsIGRpbSA9IGMoMiwzKSkKYSAqIGIKIyBvdXRlciBwcm9kdWN0CkEgPC0gYXJyYXkoMToxOCwgZGltID0gYygzLDIsMykpCkIgPC0gYXJyYXkoMTk6MzYsIGRpbSA9IGMoMiwzLDMpKQpBCkIKQUIgPC0gQSAlbyUgQgpkaW0oQUIpCmBgYAoKIyMgTWF0cml6ZW4KCk1hdHJpemVuIHNpbmQgMi1kaW1lbnNpb25hbGUgQXJyYXlzIG1pdCBiZXNvbmRlcmVuIE3DtmdsaWNoa2VpdGVuLiBMaW5lYXJlIEdsZWljaHVuZ2VuIGxhc3NlbiBzaWNoIHouQi4gbWl0IE1hdHJpemVuYXJpdGhtZXRpayBsw7ZzZW4uCgpgYGB7cn0KYU1hdHJpeCA8LSBtYXRyaXgoYygyKjE6MywgMyoxOjMpLCBucm93ID0gMiwgbmNvbCA9IDMpCmFNYXRyaXgKIyBUcmFuc3BvbmllcmVuCmFub3RoZXJNYXRyaXggPC0gdChhTWF0cml4KQojIE1hdHJpemVubXVsdGlwbGlrYXRpb24KYU1hdHJpeCAlKiUgYW5vdGhlck1hdHJpeCAKIyBLcmV1enByb2R1a3Qgdm9uIEEsIEIgPT0gdChBKSAlKiUgQgpjcm9zc3Byb2QoYU1hdHJpeCwyKjE6MikKYGBgCgoKIyMgRmFrdG9yZW4KCkVpbiBWZWt0b3Iga2FubiBpbiBGYWt0b3JlbiwgZGVuIEdydXBwZW4gZ2xlaWNoZXIgV2VydGUsIHplcmxlZ3Qgd2VyZGVuLiBEYXMgaXN0IHZlcmdsZWljaGJhciBlaW5lbSBgR1JPVVAgQllgIGluIFNRTC4KCmBgYHtyfQpzdGFkdCA8LSBjKCJCZXJsaW4iLCAiRHJlc2RlbiIsICJIYW1idXJnIiwgIkJlcmxpbiIsICJCZXJsaW4iLCAiSGFtYnVyZyIsICJEcmVzZGVuIikKa2F0ZWdvcmllIDwtIGMoIkJla2xlaWR1bmciLCAiU2NodWhlIiwgIktvc21ldGlrIiwgIktvc21ldGlrIiwgIlNjaHVoZSIsICJCZWtsZWlkdW5nIiwgIkJla2xlaWR1bmciKQpiZXRyYWcgPC0gYyg1MDAwLCA0NTAwLCAzNTAwLCAyNTAwLCAxMDAwLCAyMDAwLCA1NTAwKQpzdGFkdEFzRmFrdG9yIDwtIGZhY3RvcihzdGFkdCkKcHJpbnQoc3RhZHRBc0Zha3RvcikKYXMubnVtZXJpYyhzdGFkdEFzRmFrdG9yKQpsZXZlbHMoc3RhZHRBc0Zha3RvcikKbGV2ZWxzKHN0YWR0QXNGYWt0b3IpIDwtIGMoIkJFUiIsICJEUkUiLCAiSEFNIikKc3RhZHRDb2RlRmFrdG9yIDwtIGZhY3RvcihzdGFkdEFzRmFrdG9yLCBsYWJlbHM9YygiQiIsICJEIiwgIkgiKSkKcHJpbnQoc3RhZHRDb2RlRmFrdG9yKQp0YWJsZShzdGFkdCkKdGFwcGx5KGJldHJhZywga2F0ZWdvcmllLCBzdW0pCmBgYAoKCgoK</div>
