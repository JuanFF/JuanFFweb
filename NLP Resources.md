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

.jsonKey {
	color:#007700;
	font-size: 11pt;
}

.jsonValue {
	color:rgb(65, 65, 65);
	font-size: 11pt;
}

.jsonCodeBlock {
	margin-right: 41px;
	margin-left: 41px;
}

</style>


<p><img class = 'mainIcon' src = 'assets/algorithms.png' style="width:1.8rem;margin:0.3rem"/>NLP algorithms</p>
<ul style="list-style-type:disc;margin-left:65px;">
<li><a href="#Disease-treatment-NER">Disease-treatment NER</a></li>
<li><a href="#Healthcare-Twitter-User-Classifier">Healthcare Twitter User Classifier</a></li>
</ul>
<p><img class = 'mainIcon' src = 'assets/label.png' style="width:1.8rem;margin:0.3rem"/>Labeled datasets</p>
<ul style="list-style-type:disc;margin-left:65px;">
<li><a href="#disease-treatment-corpus">disease-treatment corpus</a></li>
<li><a href="#algorithms">healthcare twitter profiles</a></li>
<li><a href="#algorithms">performance tests</a></li>
</ul>
<br />

<hr/>

<p id="Disease-treatment-NER"><img class = 'mainIcon' src = 'assets/algorithms.png'/><b>Disease-treatment NER</b> [April 2020]</p>

<p class = 'commonP'>
	
	This is a Named Entity Recognition algorithm to extract named diseases and treatments from sentence-like text.<br /><br />

</p>

<center><img src = 'assets/resources/ner_show.gif' width="620"/></center>

<p class = 'commonP'>

	<br /><br />For the sentence<br />
	
	<code>
		Favipiravir to treat COVID-19
	</code><br /><br />
	NER will return the following<br />
	<code>
		{ <span class="jsonKey">&quot;treatment&quot;</span><span class="jsonValue">: &quot;Favipiravir&quot;,</span> <span class="jsonKey">&quot;disease&quot;</span><span class="jsonValue">: &quot;COVID-19&quot;</span> }
	</code>
	<br /><br />
	Both entities must be semantically related to be well labeled as <i>treatment</i> and <i>disease</i>; otherwise, NER will return an <code>&lt;empty&gt;</code> tag.<br /><br />
	Consider the following<br />
	<code>
		Favipiravir can't treat COVID-19
	</code><br /><br />
	The result will then be<br />
	<code>
		{ <span class="jsonKey">&quot;treatment&quot;</span><span class="jsonValue">: &quot;&lt;empty&gt;&quot;,</span> <span class="jsonKey">&quot;disease&quot;</span><span class="jsonValue">: &quot;COVID-19&quot;</span> }
	</code><br /><br />
	The algorithm precision score is 0.89. Performance varies according to text source or style. I used Twitter (healthcare-related tweets) and PubMed (research paper titles) as text sources for training and testing.<br />
</p>

<img class = 'fileIcon' src = 'assets/descargar.png'/><a href="https://github.com/JuanFF/disease-treatment-NER" target="_blank">repository</a><br />
<img class = 'fileIcon' src = 'assets/descargar.png'/><a href="https://github.com/JuanFF/datasets/tree/master/performance-tests/disease-treatment%20NER" target="_blank">test dataset</a>

<br /><br />

<hr/>

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
<img class = 'fileIcon' src = 'assets/descargar.png'/><a href="https://github.com/JuanFF/datasets/tree/master/performance-tests/healthcare%20twitter%20user%20classifier" target="_blank">test dataset</a>
<br /><br />

<hr/>

<p id="disease-treatment-corpus"><img class = 'mainIcon' src = 'assets/label.png'/><b>Corpus disease-treatment</b> [April 2020]</p>

<p class= 'commonP'>

	Find here an annotated corpus of healthcare headlines. It consists of 314620 sentence-like texts that mention one disease and its treatment. For each text, the JSON file encodes this information:<br /><br />
</p>

<pre class="jsonCodeBlock">
{ <span class="jsonKey">&quot;message&quot;</span><span class="jsonValue">: &quot;Botox as a treatment for bruxism&quot;,</span>
  <span class="jsonKey">&quot;treatment&quot;</span><span class="jsonValue">: &quot;Botox&quot;,</span>
  <span class="jsonKey">&quot;disease&quot;</span><span class="jsonValue">: &quot;bruxism&quot;,</span>
  <span class="jsonKey">&quot;source&quot;</span><span class="jsonValue">: &quot;twitter&quot;,</span>
  <span class="jsonKey">&quot;date&quot;</span><span class="jsonValue">: &quot;2018-04-22&quot;</span>  }
</pre>
	

<p class= 'commonP'>
	<br />
	<code>treatment</code> and <code>disease</code> are named entities that were automatically labeled using the <a href="#Disease-treatment-NER">disease-treatment NER</a>. The text from <code>message</code> comes from healthcare users' tweets, PubMed paper titles, and titles from studies in ClinicalTrials.gov (as specified in <code>source</code>).<br /><br />
	
	This is the frequency of each source in corpus<br />
</p>

<center><div id="piechart"></div></center>
<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
<script type="text/javascript">
google.charts.load('current', {'packages':['corechart']});
google.charts.setOnLoadCallback(drawChart);
function drawChart() {
  var data = google.visualization.arrayToDataTable([
  ['Task', 'Hours per Day'],
  ['Twitter', 8],
  ['PubMed', 2],
  ['ClinicalTrials.gov', 4],
]);
  // Optional; add a title and set the width and height of the chart
  var options = {'width':650, 'height':500};
  // Display the chart inside the <div> element with id="piechart"
  var chart = new google.visualization.PieChart(document.getElementById('piechart'));
  chart.draw(data, options);
}
</script>

<p class= 'commonP'>
	This corpus has information from 2018 and 2019. I have been working on it for training and testing the NER algorithm.<br /><br /> 
	
	All texts are publicly available on Twitter, PubMed and Clinical Trials. This corpus data is not intended for medical purposes, but for training or evaluating machine learning models.<br /><br /> 
</p>

<img class = 'fileIcon' src = 'assets/descargar.png'/><a href="https://github.com/JuanFF/datasets/tree/master/disease-treatment%20corpus" target="_blank">JSON file</a><br />
