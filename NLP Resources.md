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
<li><a href="#Healthcare-Twitter-User-Classifier">Healthcare Twitter User Classifier</a></li>
</ul>
<p><img class = 'mainIcon' src = 'assets/label.png' style="width:1.8rem;margin:0.3rem"/>Labeled datasets</p>
<ul style="list-style-type:disc;margin-left:65px;">
<li><a href="#algorithms">Healthcare Twitter User Classifier</a></li>
</ul>
<br />

- - -
<p id="Disease-treatment-NER"><img class = 'mainIcon' src = 'assets/algorithms.png'/><b>Disease-treatment NER</b> [April 2020]</p>

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
	The algorithm precision score is 0.89. Performance varies according to text source or style. I used Twitter (healthcare-related tweets) and PubMed (research paper titles) as text sources for training and testing.<br />
</p>

<img class = 'fileIcon' src = 'assets/descargar.png'/><a href="https://github.com/JuanFF/disease-treatment-NER" target="_blank">repository</a><br />
<img class = 'fileIcon' src = 'assets/descargar.png'/><a href="https://github.com/JuanFF/datasets/tree/master/performance-tests/disease-treatment%20NER" target="_blank">test dataset</a>

<br /><br />
- - -

<p id="Healthcare-Twitter-User-Classifier"><img class = 'mainIcon' src = 'assets/algorithms.png'/><b>Healthcare Twitter User Classifier</b> [April 2020]</p>

<p class = 'commonP'>

	This is a text classifier that categorizes user names and descriptions from Twitter users related to healthcare. As Twitter users provide information on themselves in their user names and descriptions, the classifier reads from this data (name, description) to return a descriptive label for each type of user profile.<br /><br />

	User profile classification may be useful when managing loads of health information on Twitter.<br /><br />

	In the following example, the classifier will return the label <code>Institution</code> to identify the profile from the World Health Organization.<br /><br />

</p>

<center><img src="assets/resources/who.png" width="550"/></center><br /><br />

<p class = 'commonP'>

	The following will return <code>Publication</code> as the label to describe this medicine journal.<br /><br />

</p>

<center><img src="assets/resources/journal.png" width="550"/></center><br /><br />

<p class= 'commonP'>
	
	In all cases, the classifier must receive the Twitter user name and description as input data. The tag set of healthcare-related profiles is the following:<br />

<ul style="margin-left: 80px;">
	<li>Academia</li>
	<li>Publishing source</li>
	<li>Doctor</li>
	<li>Professional</li>
	<li>Medical business</li>
	<li>Interested in healthcare</li>
	<li>News source</li>
	<li>Healthcare initiative</li>
	<li>Association</li>
	<li>Generic</li>
</ul>

<p class= 'commonP'>

	The classifier returns <code>&lt;empty&gt;</code> when the input profile doesn't belong to any of these categories.<br /><br />

	The precision score is 0.86<br /><br />

	Find the code, instructions and test data in the following links:<br />

</p>
<img class = 'fileIcon' src = 'assets/descargar.png'/><a href="https://github.com/JuanFF/healthcare-twitter-user-classifier" target="_blank">repository</a><br />
<img class = 'fileIcon' src = 'assets/descargar.png'/><a href="https://github.com/JuanFF/datasets/tree/master/performance-tests/healthcare%20twitter%20user%20classifier" target="_blank">test dataset</a><br />