---
permalink: /r-starter-2/
title: "R: Starter 2"
author_profile: true
layout: single-rnb
rnotebook: rnb-r-starter-2.Rmd
excerpt: "Kleine Beispiele zu Listen und Dataframes in R"
header:
        image: /assets/images/header/head_spree2.jpg
        caption: "&copy; [Kral • Photography](https://kral-photography.com)"
        twitter: /assets/images/header/head_spree2_b.jpg
date: 2017-04-20 22:44:31 +0200 
last_modified_at: 2017-04-21 00:05:15 +0200
tags: learning r variable structure
categories: language data
related: true
---

<div class="fluid-row" id="header">

<aside class="sidebar__right">
<nav class="toc flyout-toc">
<header><h4 class="nav__title"><i class="fa fa-file-alt"></i> TOC</h4></header>
<ul class="toc__menu toc_flyout" id="markdown-toc">
<li><a href="#listen">Listen</a></li>
<li><a href="#dataframes">Dataframes</a></li>
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
<div id="listen" class="section level2">
<h2>Listen</h2>
<p>Listen sind so etwas wie eine Vektor, nur das eine Liste Daten verschiedener Datentypen aufnehmen kann. Die folgende Liste besteht aus Strings, Zahlen und Vektoren. Der Liste kann ein Namens-Vektor zugeordnet werden, dessen Daten als Schlüssel der einzelnen Datenfelder verwendet werden kann.</p>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZmFtaWxpZSA8LSBsaXN0KFwiTWFtYVwiLFwiUGFwYVwiLCBjKFwiS2lkMVwiLFwiS2lkMlwiLFwiS2lkM1wiKSwzLGMoNCw1LDcpKVxubmFtZXMoZmFtaWxpZSkgPC0gYyhcIk11dHRlclwiLFwiVmF0ZXJcIixcIktpbmRlclwiLFwiV2lldmllbGUgS2luZGVyXCIsXCJBbHRlciBkZXIgS2luZGVyXCIpXG5mYW1pbGllWzFdXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">familie &lt;-<span class="st"> </span><span class="kw">list</span>(<span class="st">&quot;Mama&quot;</span>,<span class="st">&quot;Papa&quot;</span>, <span class="kw">c</span>(<span class="st">&quot;Kid1&quot;</span>,<span class="st">&quot;Kid2&quot;</span>,<span class="st">&quot;Kid3&quot;</span>),<span class="dv">3</span>,<span class="kw">c</span>(<span class="dv">4</span>,<span class="dv">5</span>,<span class="dv">7</span>))
<span class="kw">names</span>(familie) &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;Mutter&quot;</span>,<span class="st">&quot;Vater&quot;</span>,<span class="st">&quot;Kinder&quot;</span>,<span class="st">&quot;Wieviele Kinder&quot;</span>,<span class="st">&quot;Alter der Kinder&quot;</span>)
familie[<span class="dv">1</span>]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiJE11dHRlclxuWzFdIFwiTWFtYVwiXG4ifQ== -->
<pre><code>$Mutter
[1] &quot;Mama&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZmFtaWxpZVtbMV1dXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">familie[[<span class="dv">1</span>]]</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiTWFtYVwiXG4ifQ== -->
<pre><code>[1] &quot;Mama&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZmFtaWxpZSRNdXR0ZXJcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">familie$Mutter</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiTWFtYVwiXG4ifQ== -->
<pre><code>[1] &quot;Mama&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-chunk-end -->
<!-- rnb-text-begin -->
</div>
<div id="dataframes" class="section level2">
<h2>Dataframes</h2>
<p>Dataframes sind so ähnlich wie Matrizen und bestehen aus Vektoren mit Daten verschiedener Datentypen. Dataframes können über eine Variable zusammengeführt – gemerged – werden. Das entspricht in etwa einem JOIN in SQL.</p>
<!-- rnb-text-end -->
<!-- rnb-chunk-begin -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxucGFydGljbGVOYW1lcyA8LSBjKFwiQWxpY2VcIixcIkJvYlwiLFwiQ29yYVwiLFwiRGF2ZVwiLFwiRW1tYVwiLFwiRnJhbmtcIilcbnR5cGVzIDwtIGMoXCJQaG90b25cIixcIlBob3RvblwiLFwiTmV1dHJvblwiLFwiUHJvdG9uXCIsXCJFbGVrdHJvblwiLFwiUGhvdG9uXCIpXG5zcGlucyA8LSBjKDEyMCwgMTA4LCA5OCwgNDUsIDExNSwgMTAwKVxucGFydGljbGVJbmZvIDwtIGRhdGEuZnJhbWUocGFydGljbGVOYW1lcywgdHlwZXMsIHNwaW5zKVxucGFydGljbGVJbmZvXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">particleNames &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;Alice&quot;</span>,<span class="st">&quot;Bob&quot;</span>,<span class="st">&quot;Cora&quot;</span>,<span class="st">&quot;Dave&quot;</span>,<span class="st">&quot;Emma&quot;</span>,<span class="st">&quot;Frank&quot;</span>)
types &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="st">&quot;Photon&quot;</span>,<span class="st">&quot;Photon&quot;</span>,<span class="st">&quot;Neutron&quot;</span>,<span class="st">&quot;Proton&quot;</span>,<span class="st">&quot;Elektron&quot;</span>,<span class="st">&quot;Photon&quot;</span>)
spins &lt;-<span class="st"> </span><span class="kw">c</span>(<span class="dv">120</span>, <span class="dv">108</span>, <span class="dv">98</span>, <span class="dv">45</span>, <span class="dv">115</span>, <span class="dv">100</span>)
particleInfo &lt;-<span class="st"> </span><span class="kw">data.frame</span>(particleNames, types, spins)
particleInfo</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-frame-begin eyJtZXRhZGF0YSI6eyJjbGFzc2VzIjpbImRhdGEuZnJhbWUiXSwibmNvbCI6MywibnJvdyI6Nn0sInJkZiI6Ikg0c0lBQUFBQUFBQUEzMVMzVTdDTUJRK1d6ZVFKYUFKejhFdWVBSlU0SklZcnpBWWt6S0tMSlIyNlFycW5ZL21rNEg5T2RXQmlVMjJjNzd2L1BmMGNUd2Zadk1NQUdJZ2hFQk1qSnJFNWhkQkFoMHIzd0ZJM3lqR1FycEd0cHpSQmpqT3VBR2tuajhMYkhGMllMdzIybzJ6ZWphOTVXWEJFSkE3dVVRMXVaZUtCbjFNRDhFbG1leDJnVStuaW9ydFJabTA0TFFPVlg1cXIybWhwVExhc2RFMXdTL0dyaU9QYmJyNGhCa1N6SEExNFd5cmxSU0kyek8yYjhEV3cwYnFCbElPdVZUazlGOHowTFBNNkFYY0dTMVF6ais5bktKOC92THlDZkNjenl6b2pvV1pDWkxkaWlwZEZwek5uQkU5OVVmMUMrcXFGUFZGcm82U2IzbklaMjhxOWkyRWZmNFpKMXRSVGZPMU1pRitwTE4wYlZucFV0b3FjUjhmUmpNNFVoZkU5VjdZNHF0QnNkbUw3V0JvQytCcUFCdUtjSDFCeDVVbG9iRTAzRE1UcjZVSUR5ZmxkTWs0Z3A0WjBzMllWNm9VT2t4aTJEclhVdFBnbHhXU0I4YXY2L2dOSXpSMDd5SURBQUE9In0= -->
<div data-pagedtable="false">
<script data-pagedtable-source type="application/json">
{"columns":[{"label":["particleNames"],"name":[1],"type":["fctr"],"align":["left"]},{"label":["types"],"name":[2],"type":["fctr"],"align":["left"]},{"label":["spins"],"name":[3],"type":["dbl"],"align":["right"]}],"data":[{"1":"Alice","2":"Photon","3":"120"},{"1":"Bob","2":"Photon","3":"108"},{"1":"Cora","2":"Neutron","3":"98"},{"1":"Dave","2":"Proton","3":"45"},{"1":"Emma","2":"Elektron","3":"115"},{"1":"Frank","2":"Photon","3":"100"}],"options":{"columns":{"min":{},"max":[10],"total":[3]},"rows":{"min":[10],"max":[10],"total":[6]},"pages":{}}}
  </script>
</div>
<!-- rnb-frame-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaGVhZChwYXJ0aWNsZUluZm8sMylcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">head</span>(particleInfo,<span class="dv">3</span>)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-frame-begin eyJtZXRhZGF0YSI6eyJjbGFzc2VzIjpbImRhdGEuZnJhbWUiXSwibmNvbCI6MywibnJvdyI6M30sInJkZiI6Ikg0c0lBQUFBQUFBQUEzMVN3VTdETUF4TmszWmpsVGFRK0k3MXNDOFlzSEdjRUtkS1NFaFpsN0dxYVZLbDZZQWJYNzZSdERaMGxhQlM2dmNjMjg5TzhyeEtGM0VhRTBJb1lZd1J5aHdNcWZzRkpDUVRiejhJWWJjT3VCMDI3YXpiOUFrdHZnZ2VTWEVVc25ib3hqUHdSbmN5endRUWRxKzNBTU1IYlRqaUZUOWlTTGd1Uy9SSGo0YXJZaUFUWlpMWHFQS2p2ZWVaMWNhaFU2OVRYTFFyUWMrUUZVTFcxVnFLd2hxdGdJODNvdW5SMGROQjJ4NHpMV3RMc2ZOL0RaQ1pGMTYra3ZaYnZvQk52em93bUVmeFV1QThESnpUaWh1YloxSnMyazJJdEovVkw2bXJYTldEV2hPajN4T3M1MCtCZ2lUN28rMTR4eTFQOXNhbGRLMWZsQnZyeXViYXExRC9DS0pCY21BR2p1dEdlZkhkUERzMHFwZ3Z2QUE4bUFBYUN1QktldGhMaHRoWWhPY3AxRnV1OEZGRWttK0ZCREp6UTdZekpwWEpsY1ZKbkxkT3JMWWM0K0pNUy9SMDEzTDZCb0x4eUVieUFnQUEifQ== -->
<div data-pagedtable="false">
<script data-pagedtable-source type="application/json">
{"columns":[{"label":[""],"name":["_rn_"],"type":[""],"align":["left"]},{"label":["particleNames"],"name":[1],"type":["fctr"],"align":["left"]},{"label":["types"],"name":[2],"type":["fctr"],"align":["left"]},{"label":["spins"],"name":[3],"type":["dbl"],"align":["right"]}],"data":[{"1":"Alice","2":"Photon","3":"120","_rn_":"1"},{"1":"Bob","2":"Photon","3":"108","_rn_":"2"},{"1":"Cora","2":"Neutron","3":"98","_rn_":"3"}],"options":{"columns":{"min":{},"max":[10],"total":[3]},"rows":{"min":[10],"max":[10],"total":[3]},"pages":{}}}
  </script>
</div>
<!-- rnb-frame-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubnJvdyhwYXJ0aWNsZUluZm8pXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">nrow</span>(particleInfo)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDZcbiJ9 -->
<pre><code>[1] 6</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubmNvbChwYXJ0aWNsZUluZm8pXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">ncol</span>(particleInfo)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDNcbiJ9 -->
<pre><code>[1] 3</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxubmFtZXMocGFydGljbGVJbmZvKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">names</span>(particleInfo)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwicGFydGljbGVOYW1lc1wiIFwidHlwZXNcIiAgICAgICAgIFwic3BpbnNcIiAgICAgICAgXG4ifQ== -->
<pre><code>[1] &quot;particleNames&quot; &quot;types&quot;         &quot;spins&quot;        </code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxucm93bmFtZXMocGFydGljbGVJbmZvKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">rownames</span>(particleInfo)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwiMVwiIFwiMlwiIFwiM1wiIFwiNFwiIFwiNVwiIFwiNlwiXG4ifQ== -->
<pre><code>[1] &quot;1&quot; &quot;2&quot; &quot;3&quot; &quot;4&quot; &quot;5&quot; &quot;6&quot;</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuY29sbmFtZXMocGFydGljbGVJbmZvKVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">colnames</span>(particleInfo)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIFwicGFydGljbGVOYW1lc1wiIFwidHlwZXNcIiAgICAgICAgIFwic3BpbnNcIiAgICAgICAgXG4ifQ== -->
<pre><code>[1] &quot;particleNames&quot; &quot;types&quot;         &quot;spins&quot;        </code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZGltKHBhcnRpY2xlSW5mbylcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="kw">dim</span>(particleInfo)</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-output-begin eyJkYXRhIjoiWzFdIDYgM1xuIn0= -->
<pre><code>[1] 6 3</code></pre>
<!-- rnb-output-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuIyBNZXJnZSBEYXRhZnJhbWVzXG5kZjEgPC0gZGF0YS5mcmFtZShjdXN0SWQgPSAxOjMsIGN1c3ROYW1lID0gYyhcIkpvaG5cIixcIkphbmlzXCIsXCJKYW1lc1wiKSlcbmRmMVxuYGBgIn0= -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r"><span class="co"># Merge Dataframes</span>
df1 &lt;-<span class="st"> </span><span class="kw">data.frame</span>(<span class="dt">custId =</span> <span class="dv">1</span>:<span class="dv">3</span>, <span class="dt">custName =</span> <span class="kw">c</span>(<span class="st">&quot;John&quot;</span>,<span class="st">&quot;Janis&quot;</span>,<span class="st">&quot;James&quot;</span>))
df1</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-frame-begin eyJtZXRhZGF0YSI6eyJjbGFzc2VzIjpbImRhdGEuZnJhbWUiXSwibmNvbCI6MiwibnJvdyI6M30sInJkZiI6Ikg0c0lBQUFBQUFBQUEyVlF5MDdETUJEY2VCT2drWGhJZkVkejZEZHdvUWNPbkhvMWlkdEdHTHV5SGVESWx4Zldqd1hKUkVxeU01NGQ3K3p6dzI3VDczb0FFSUNJSUpES1Z0Q25nUlpXOGY4SmdQZEpBSEJOTDZiRGpLbEc1ckJ3VFdWd29kVzcwcDZxdTZUS2JMZVZiOHIvQVRNemFMZjJhQ3FQYnRUU3M4V3Y4VjZPd1RxcXpyWGNKUE1zRnl3ZkZ4OGVwNEt1SW5vaVdkVzZjdlpqNFBZWVRYeEJlakFMOGJ1YW9wOWtrTVBlSmF0L2sxemFVNWl0SVRNUmQ5aFZ6WTJyaU52RnhNdW45WGhjek90NkV5OG8rNFl5VUZOMnpiWElWN1k4V01kNWxUbk1SdkZLdEh4UnVvQWJDcGt5RGljM204QkppUFZEc0VHeXJoK3RaaVpsZy9NUFVaSkNjekVDQUFBPSJ9 -->
<div data-pagedtable="false">
<script data-pagedtable-source type="application/json">
{"columns":[{"label":["custId"],"name":[1],"type":["int"],"align":["right"]},{"label":["custName"],"name":[2],"type":["fctr"],"align":["left"]}],"data":[{"1":"1","2":"John"},{"1":"2","2":"Janis"},{"1":"3","2":"James"}],"options":{"columns":{"min":{},"max":[10],"total":[2]},"rows":{"min":[10],"max":[10],"total":[3]},"pages":{}}}
  </script>
</div>
<!-- rnb-frame-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZGYyIDwtIGRhdGEuZnJhbWUoY3VzdElkID0gMTozLCBjdXN0QWdlID0gYygzNiwzNiwyNikpXG5kZjJcbmBgYCJ9 -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">df2 &lt;-<span class="st"> </span><span class="kw">data.frame</span>(<span class="dt">custId =</span> <span class="dv">1</span>:<span class="dv">3</span>, <span class="dt">custAge =</span> <span class="kw">c</span>(<span class="dv">36</span>,<span class="dv">36</span>,<span class="dv">26</span>))
df2</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-frame-begin eyJtZXRhZGF0YSI6eyJjbGFzc2VzIjpbImRhdGEuZnJhbWUiXSwibmNvbCI6MiwibnJvdyI6M30sInJkZiI6Ikg0c0lBQUFBQUFBQUExMVFQUS9DSUJDOWd0VzBpUitKdjhNT2prNXFYRnlkWExGRmJhelF0RFE2K3N2VmczSW1RZ0ozNzhHN3U4ZGhkMXlteHhRQUdIRE9nWEZNQnd5UENBYVEyUGdFNEhQM0FHQ01tN3ZMSHR0OFl1TjZDMjc5NGdyOCtpc1dLM0dYTFNZelY2QW5oM25YbW4zaDBjaWl6VVVHeXFUUmo0elVkZ3oyNnV2enNFVmVpWlphRUprV3dvanMzS0FlMFR1UWpIUnRTcTFReEt6Uk9CQkhUVUJNTzJVbktSYjV0Vk8zeGRJMjhKOENmcnJJZnc3bHJHL0pQcjVVVE42bHVwUkswdXlWT01uS2d3azZkb2F6dWltVklTZkl0cG5SUnRDN05OY1ZNYzRidkw5Qk9ndUQxZ0VBQUE9PSJ9 -->
<div data-pagedtable="false">
<script data-pagedtable-source type="application/json">
{"columns":[{"label":["custId"],"name":[1],"type":["int"],"align":["right"]},{"label":["custAge"],"name":[2],"type":["dbl"],"align":["right"]}],"data":[{"1":"1","2":"36"},{"1":"2","2":"36"},{"1":"3","2":"26"}],"options":{"columns":{"min":{},"max":[10],"total":[2]},"rows":{"min":[10],"max":[10],"total":[3]},"pages":{}}}
  </script>
</div>
<!-- rnb-frame-end -->
<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuZGYzIDwtIG1lcmdlKGRmMSwgZGYyLCBieT1cImN1c3RJZFwiKVxuZGYzXG5gYGAifQ== -->
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">df3 &lt;-<span class="st"> </span><span class="kw">merge</span>(df1, df2, <span class="dt">by=</span><span class="st">&quot;custId&quot;</span>)
df3</code></pre></div>
<!-- rnb-source-end -->
<!-- rnb-frame-begin eyJtZXRhZGF0YSI6eyJjbGFzc2VzIjpbImRhdGEuZnJhbWUiXSwibmNvbCI6MywibnJvdyI6M30sInJkZiI6Ikg0c0lBQUFBQUFBQUExMVJUVlBESUJCZElQUWpNMVpuL0IzTm9VZFA2bml4QncrZWVrVkMyNHdVT2tEVW83KzhDZ1RhQm1hUzNmZFkzcjZGOTVmTnF0N1VBSUNCRUFLWStMVEMvb2VnZ25tSVB3RGszaWRoNXlaRkZBL0VuR1NPSkE0VkFoTXB2b1MwUHJ1TFZRTkwxK3dnN0FXb0xvTnFyZmVxMEtCY01wc2x6c0pieHAwMlBqdjVieEhFSDU4aHJuTjhnTFRHY2lvMkh6dWE4TjY2MXphaFdVQnZ2aXpoYWNCUE8xRW96WTMrYnJKYXVBbjhPL1FqUXlINUswelhMWE9zMlpxZ0hJMlA1S2I2NkRxdHZCZ09WMDZMdzhnVXhHMnZRdk4yeWZlOStseXVRb1AwUEpBTW9hdW5ReGRqVlRaRzgvaEM3VHFWeDZXU2ZRaVp3TUlQR1dkc2pxWlRMay9pV2RzNDdWaXVxN21XbVJrZTVmUVA3a1RhZldBQ0FBQT0ifQ== -->
<div data-pagedtable="false">
<script data-pagedtable-source type="application/json">
{"columns":[{"label":["custId"],"name":[1],"type":["int"],"align":["right"]},{"label":["custName"],"name":[2],"type":["fctr"],"align":["left"]},{"label":["custAge"],"name":[3],"type":["dbl"],"align":["right"]}],"data":[{"1":"1","2":"John","3":"36"},{"1":"2","2":"Janis","3":"36"},{"1":"3","2":"James","3":"26"}],"options":{"columns":{"min":{},"max":[10],"total":[3]},"rows":{"min":[10],"max":[10],"total":[3]},"pages":{}}}
  </script>
</div>
<!-- rnb-frame-end -->
<!-- rnb-chunk-end -->
<!-- rnb-text-begin -->
<!-- rnb-text-end -->
</div>

<div id="rmd-source-code">LS0tCnRpdGxlOiAiUjogU3RhcnRlciAyIgpvdXRwdXQ6CiAgaHRtbF9ub3RlYm9vazoKICAgIGNvZGVfZm9sZGluZzogbm9uZQogICAgZGZfcHJpbnQ6IGthYmxlCiAgICBoaWdobGlnaHQ6IHB5Z21lbnRzCiAgICB0aGVtZTogZmxhdGx5CiAgICB0b2M6IHllcwogIGh0bWxfZG9jdW1lbnQ6CiAgICBoaWdobGlnaHQ6IHB5Z21lbnRzCiAgICBrZWVwX21kOiB5ZXMKLS0tCgojIyBMaXN0ZW4KCkxpc3RlbiBzaW5kIHNvIGV0d2FzIHdpZSBlaW5lIFZla3RvciwgbnVyIGRhcyBlaW5lIExpc3RlIERhdGVuIHZlcnNjaGllZGVuZXIgRGF0ZW50eXBlbiBhdWZuZWhtZW4ga2Fubi4gRGllIGZvbGdlbmRlIExpc3RlIGJlc3RlaHQgYXVzIFN0cmluZ3MsIFphaGxlbiB1bmQgVmVrdG9yZW4uIERlciBMaXN0ZSBrYW5uIGVpbiBOYW1lbnMtVmVrdG9yIHp1Z2VvcmRuZXQgd2VyZGVuLCBkZXNzZW4gRGF0ZW4gYWxzIFNjaGzDvHNzZWwgZGVyIGVpbnplbG5lbiBEYXRlbmZlbGRlciB2ZXJ3ZW5kZXQgd2VyZGVuIGthbm4uCgpgYGB7cn0KZmFtaWxpZSA8LSBsaXN0KCJNYW1hIiwiUGFwYSIsIGMoIktpZDEiLCJLaWQyIiwiS2lkMyIpLDMsYyg0LDUsNykpCm5hbWVzKGZhbWlsaWUpIDwtIGMoIk11dHRlciIsIlZhdGVyIiwiS2luZGVyIiwiV2lldmllbGUgS2luZGVyIiwiQWx0ZXIgZGVyIEtpbmRlciIpCmZhbWlsaWVbMV0KZmFtaWxpZVtbMV1dCmZhbWlsaWUkTXV0dGVyCmBgYAoKIyMgRGF0YWZyYW1lcwoKRGF0YWZyYW1lcyBzaW5kIHNvIMOkaG5saWNoIHdpZSBNYXRyaXplbiB1bmQgYmVzdGVoZW4gYXVzIFZla3RvcmVuIG1pdCBEYXRlbiB2ZXJzY2hpZWRlbmVyIERhdGVudHlwZW4uIERhdGFmcmFtZXMga8O2bm5lbiDDvGJlciBlaW5lIFZhcmlhYmxlIHp1c2FtbWVuZ2Vmw7xocnQgLS0gZ2VtZXJnZWQgLS0gd2VyZGVuLiBEYXMgZW50c3ByaWNodCBpbiBldHdhIGVpbmVtIEpPSU4gaW4gU1FMLgoKYGBge3J9CnBhcnRpY2xlTmFtZXMgPC0gYygiQWxpY2UiLCJCb2IiLCJDb3JhIiwiRGF2ZSIsIkVtbWEiLCJGcmFuayIpCnR5cGVzIDwtIGMoIlBob3RvbiIsIlBob3RvbiIsIk5ldXRyb24iLCJQcm90b24iLCJFbGVrdHJvbiIsIlBob3RvbiIpCnNwaW5zIDwtIGMoMTIwLCAxMDgsIDk4LCA0NSwgMTE1LCAxMDApCnBhcnRpY2xlSW5mbyA8LSBkYXRhLmZyYW1lKHBhcnRpY2xlTmFtZXMsIHR5cGVzLCBzcGlucykKcGFydGljbGVJbmZvCmhlYWQocGFydGljbGVJbmZvLDMpCm5yb3cocGFydGljbGVJbmZvKQpuY29sKHBhcnRpY2xlSW5mbykKbmFtZXMocGFydGljbGVJbmZvKQpyb3duYW1lcyhwYXJ0aWNsZUluZm8pCmNvbG5hbWVzKHBhcnRpY2xlSW5mbykKZGltKHBhcnRpY2xlSW5mbykKCiMgTWVyZ2UgRGF0YWZyYW1lcwpkZjEgPC0gZGF0YS5mcmFtZShjdXN0SWQgPSAxOjMsIGN1c3ROYW1lID0gYygiSm9obiIsIkphbmlzIiwiSmFtZXMiKSkKZGYxCmRmMiA8LSBkYXRhLmZyYW1lKGN1c3RJZCA9IDE6MywgY3VzdEFnZSA9IGMoMzYsMzYsMjYpKQpkZjIKZGYzIDwtIG1lcmdlKGRmMSwgZGYyLCBieT0iY3VzdElkIikKZGYzCmBgYAoK</div>