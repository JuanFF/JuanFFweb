---
layout: home
title: NLP Resources
---

<style>
.mainIcon {
	vertical-align:text-bottom;
	width:1.8rem;
	margin-right: 0.7rem;
}
.fileIcon {
	vertical-align:text-bottom;
	width:1.2rem;
	margin-left:41px;
	margin-right:7px;
}
.commonP {
	margin-left:41px;
}
</style>



<p><img class = 'mainIcon' src = 'assets/algorithms.png' style="width:1.8rem;margin:0.3rem"/>NLP algorithms</p>
<ul style="list-style-type:disc;margin-left:65px;">
<li><a href="#Disease-treatment-NER">Disease-treatment NER</a></li>
<li><a href="#Health-worker-classifier">Health worker classifier</a></li>
</ul>
<p><img class = 'mainIcon' src = 'assets/label.png' style="width:1.8rem;margin:0.3rem"/>Labeled datasets</p>
<ul style="list-style-type:disc;margin-left:65px;">
<li><a href="#algorithms">Disease-treatment Twitter dataset</a></li>
</ul>
<p><img class = 'mainIcon' src = 'assets/bulbo.png' style="width:1.8rem;margin:0.3rem"/>Data insights</p>
<ul style="list-style-type:disc;margin-left:65px;">
<li><a href="#algorithms">Lifescope stats</a></li>
</ul>
<br />

- - -
<p><img class = 'mainIcon' src = 'assets/algorithms.png'/><b>Disease-treatment NER</b> [April 2020]</p>

<p class = 'commonP'>

	This is a Named Entity Recognition algorithm to extract named diseases and treatments from sentence-like text.<br /><br />
	For the sentence<br />
	<code>
		Favipiravir to treat COVID-19
	</code><br /><br />
	NER will return the following<br />
	<code>
		{&quot;treatment&quot;: &quot;Favipiravir&quot;, &quot;disease&quot;: &quot;COVID-19&quot;}
	</code><br /><br />
	Both entities must be semantically related to be well labeled as <i>treatment</i> and <i>disease</i>; otherwise, NER will return an <code>&lt;empty&gt;</code> tag.<br /><br />
	Consider the following<br />
	<code>
		Favipiravir can't treat COVID-19
	</code><br /><br />
	The result will then be<br />
	<code>
		{&quot;treatement&quot;: &quot;&lt;empty&gt;&quot;, &quot;disease&quot;: &quot;COVID-19&quot;}
	</code><br /><br />
	The algorithm precision score is 0.89 (0.83 for treatment entity recognition, and 0.96 for disease entities). Performance varies according to text source or style. I used Twitter (healthcare-related tweets) and PubMed (research paper titles) as text sources for training and testing.<br />
</p>

<img class = 'fileIcon' src = 'assets/github.png'/><a href="https://github.com/JuanFF/disease-treatment-NER" target="_blank">repository</a><br />
<img class = 'fileIcon' src = 'assets/github.png'/><a href="https://github.com/JuanFF/datasets/tree/master/performance-tests" target="_blank">test dataset</a>