---
layout: home
title: Apps
---


<style>

.spinners-container .spinner-block {
    float:none;
		width:1.3rem;
		margin-left:0px;
		margin-right:8px;
    vertical-align:text-bottom;
}
.spinners-container .spinner-block:nth-child(5n) {
  margin-right: 0px;
}
.spinners-container .spinner-block h2 {
  margin: 0px 0px 20px 0px;
}

/* YOU NEED THESE STYLES */
/* spinner style */
.spinner-eff {
  position: relative;
  width: 40px;
  height: 40px;
}
.spinner-eff:before, .spinner-eff:after {
  content: "";
  display: block;
}
.spinner-eff .spinner-bar:before, .spinner-eff .spinner-bar:after {
  content: "";
  display: block;
}


/* spinner-3 styles */
@-webkit-keyframes pulse {
  0% {
    -webkit-transform: scale(0);
            transform: scale(0);
  }
  50% {
    -webkit-transform: scale(1.3);
            transform: scale(1.3);
    opacity: 0;
  }
  100% {
    -webkit-transform: scale(1.3);
            transform: scale(1.3);
    opacity: 0;
  }
}
@keyframes pulse {
  0% {
    -webkit-transform: scale(0);
            transform: scale(0);
  }
  50% {
    -webkit-transform: scale(1.3);
            transform: scale(1.3);
    opacity: 0;
  }
  100% {
    -webkit-transform: scale(1.3);
            transform: scale(1.3);
    opacity: 0;
  }
}
@-webkit-keyframes pulse-2 {
  0% {
    -webkit-transform: scale(0);
            transform: scale(0);
  }
  100% {
    -webkit-transform: scale(1.3);
            transform: scale(1.3);
    opacity: 0;
  }
}
@keyframes pulse-2 {
  0% {
    -webkit-transform: scale(0);
            transform: scale(0);
  }
  100% {
    -webkit-transform: scale(1.3);
            transform: scale(1.3);
    opacity: 0;
  }
}
.spinner-eff.spinner-eff-3 .circle {
  border-radius: 100px;
  position: absolute;
  left: 0;
  right: 0;
  margin: auto;
  -webkit-transform: scale(1);
          transform: scale(1);
  -webkit-transform-origin: center center;
          transform-origin: center center;
}
.spinner-eff.spinner-eff-3 .circle-1 {
  width: 100%;
  height: 100%;
  background-color: #60f691;
  top: 0;
  -webkit-animation: pulse 1.9s linear 0s infinite;
          animation: pulse 1.9s linear 0s infinite;
}
.spinner-eff.spinner-eff-3 .circle-2 {
  width: 66.6%;
  height: 66.6%;
  background-color: #0CCA4A;
  top: 16.5%;
  -webkit-animation: pulse-2 1.9s linear 0s infinite;
          animation: pulse-2 1.9s linear 0s infinite;
}
.spinner-eff.spinner-eff-3 .circle-3 {
  width: 33.3%;
  height: 33.3%;
  background-color: #0CCA4A;
  top: 33.3%;
}



.commonP {
	margin-left:50px;
}

.section-icon {
	width:2.15rem;
	margin-right:0.9rem;
  margin-left:2.9rem;
	vertical-align:text-bottom;
}



@media only screen and (max-width: 1024px) {
  .prev, .next,.text {font-size: 11px}
	.commonP {
		margin-left:0px;
	}
  .section-icon {
	width:2.15rem;
	margin-right:0.5rem;
  margin-left:0rem;
	vertical-align:text-bottom;
  }
}

</style>

<br/>

<h2><img src = 'assets/enfermero.png' class = 'section-icon'/>Buenas noticias COVID</h2>

<p class = 'commonP'>

	En mayo del 2020, programé un bot que analizaba, en tiempo real, titulares en Twitter para recuperar las noticias en positivo sobre la pandemia. Hace tiempo que desconecté el bot con la esperanza de que todas las  noticias sobre la pandemia tuvieran que ver, casi exclusivamente, con las vacunas. No obstante, dejo aquí el timeline original para cualquiera que tenga interés en saber cómo evolucionaron las buenas noticias en los primeros seis meses de la pandemia.
  <br/><br/>
  El bot analizaba no solo el contenido, sino también el emisor, para hacer retweet solo de fuentes escogidas: las cuentas verificadas por Twitter, o las que él identificaba como usuarios que tienen relación con la sanidad.
	<br/><br/>
  Tiene una precisión de 0.89. Código disponible en <a href="https://github.com/JuanFF/fight_covid_classifier" target="_blank">repositorio</a>.
  <br/><br/>
	<a style="text-align:left" href="https://twitter.com/venceralcovid?ref_src=twsrc%5Etfw" class="twitter-follow-button" data-show-count="false">Follow @venceralcovid</a><script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> <br/>
</p>

<br/>

<center>
  <div class="spinner-block" title="Listening good news">
    <div class="spinner-eff spinner-eff-3">
      <div class="circle circle-1"></div>
      <div class="circle circle-2"></div>
      <div class="circle circle-3"></div>
    </div>
  </div>

  <a class="twitter-timeline" data-width="650" href="https://twitter.com/venceralcovid?ref_src=twsrc%5Etfw"></a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>

