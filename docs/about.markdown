---
layout: page
title: Research
image: assets/images/dtb_10000signals-1.png
nav-menu: true
show_tile: true
nav_order: 1
---

<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>Research</h1>
		</header>

<p> My research consists in numerical studies of the Epoch of Reionisation (EoR). The 21-cm signal of neutral Hydrogen is an extremely promising
probe of the first billion years of the Universe, and the The Square Kilometer Array (SKA), a radio-interferometer of
incredible sensitivity currently under construction, should be able to provide a map of the intensity of the
21-cm signal in the whole sky in the 2030’s. However, two main challenges remain regarding the interpretation of current and future 21-cm observations, and my research addresses both facets.
</p>


<!-- Content -->
<h2 id="simu">Accurate cosmological simulations...</h2>
<p> Modelling the EoR and the 21-cm signal is physically complex and can be computationally expensive. I have contributed to the development of Licorice, an N-body, hydro-radiative cosmological simulation code. I have implemented subgrid models affecting star formation and X-ray heating which make the code accurate at low resolution, and therefore low cost: only a few hundred CPU-hours at 256<sup>3</sup> resolution, an unprecedented result for 3D radiative transfer simulations of the 21-cm signal.  </p>
<div class="row">
	<div class="6u 12u$(small)">
		<h3>The Loreli II database</h3>
		<p> Thanks to this relatively low cost, I have run Loreli I, a database of 760 models, as well as its update, Loreli II, which contains nearly 10 000 Licorice simulations. It is a massive HPC project containing 10000 simulations spanning a 5D parameter space and weighing ∼ 1.5 PB of data. This dataset remains the only one in its category and opens the possibility of training machine learning models on 3D RT simulations of the EoR. 
		Summary statistics of Loreli II simulations can be found  <a href="https://21ssd.obspm.fr/" target="_blank" rel="noopener noreferrer"> <strong> here</strong></a>, and more complex data is available on request.  </p>
	</div>
	<div class="6u$ 12u$(small)">
		<h3> Do different codes agree with one another?</h3>
		<p>Another of my interests is the agrement between predictions of different simulation codes used by the 21-cm community. Among other works, the <a href="https://sdc3.skao.int/challenges/inference/results" target="_blank" rel="noopener noreferrer"> <strong> SDC3b</strong></a> suggests that model misspecifications (using model A to interpret data generated with model B) may prove a significant obstacle. To tackle this, I have performed a thorough comparison of the radiative transfer schemes used in Licorice (3DRT) and Beorn (1DRT), and explored the impact of different physical approximations commonly used throughout the community. I believe that additional code comparisons are essential before we can provide reliable interpretations of SKA data. </p>
	</div>
</div>

<h2 id="bayes">... and using them with AI</h2>
<p> Beyond simulation codes and High-Performance Computing, I use advanced AI models to bridge the gap between simulations and observations. Naturally, Loreli II provides an excellent training sample for those models. </p>
<div class="row">
	<div class="6u 12u$(small)">
		<h3>Bayesian Inference: Likelihood- and Simulation-based methods</h3>
		<p> The likelihood function of most summary statistics of the signal cannot be expressed analytically. When such expressions exist, they are often approximate. To validate these approximations or bypass them when necessary, I have compared Likelihood-Based Inference with Simulation-Based techniques. The former relies on an ML emulator of the Loreli II power spectra and a Gaussian Likelihood, while the latter relies on learning the likelihood or posterior distributions directly. Fortunately, all three methods largely agree, indicating that this final step of the SKA interpretation pipeline is unlikely to be a show-stopper. Additionally, we provide the first interpretation of power spectrum upper limits (provided by HERA) with 3D RT simulations, and work towards interpretation of NenuFAR data with updated models. </p>
	</div>
	<div class="6u$ 12u$(small)">
		<h3>Full lightcone emulation with Lorelight</h3>
		<p>Even with subgrid models, 3D radiative transfer simulations remain more expensive and less flexible than semi-numerical methods. I have trained Lorelight, a complex neural network that predicts the thermodynamical state of the IGM given a density field and the luminosities of the corresponding galaxies. In other words, Lorelight learns the radiative transfer scheme used in Loreli II. Lorelight generalises well to unseen star formation models, and can therefore be applied to galaxies simulated with efficient schemes, such as particle-mesh methods. Lorelight might be a way towards getting the best of both worlds : fast and flexible galaxy formation models while retaining the benefits of 3D radiative transfer, in one single cheap and GPU-friendly package.</p>
	</div>
</div>

<p> I have chosen to highlight some results here, but you can find a complete list of publications in the corresponding section of this website.  </p>

	</div>
</section>
</div>
