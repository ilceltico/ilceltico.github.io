---
layout: paper
title: "S2MDF"
permalink: /papers/2026/s2mdf/
description: "S2MDF: A Plug-And-Play Layer for Intersection-Free Multi-Object Signed Distance Fields"
image: /assets/previews/s2mdf.jpg
---

<style>
.s2mdf-video { width: 100%; display: block; border-radius: 10px; margin: 5px 0; }
.s2mdf-labels { display: flex; text-align: center; font-weight: bold; font-size: 15px; }
.s2mdf-labels div { flex: 1; }
.s2mdf-results h3 { margin: 28px 0 2px 0; }
.s2mdf-results .note { color: #777; font-size: 14px; margin-bottom: 4px; }
.s2mdf-legend { text-align: center; font-size: 15px; color: #555; margin-top: 4px; }
.s2mdf-legend span { display: inline-block; width: 14px; height: 14px; border-radius: 3px; vertical-align: -2px; margin: 0 5px 0 14px; }

/* LaTeX-style (booktabs) results table, overriding the site-wide table style */
.booktabs { width: 100%; border-collapse: collapse; margin: 6px 0 18px 0; font-size: 15px; }
.booktabs tr:nth-child(even) { background: none; }
.booktabs th, .booktabs td { background: none; border: 0; padding: 4px 8px; width: auto; text-align: right; white-space: nowrap; }
.booktabs th:first-child, .booktabs td:first-child { text-align: left; }
.booktabs thead tr:first-child th { border-top: 2px solid #222; }
.booktabs thead tr:last-child th { border-bottom: 1px solid #222; }
.booktabs tbody tr:last-child td { border-bottom: 2px solid #222; }
.booktabs .group td { font-weight: bold; text-align: left; padding-top: 10px; }
.booktabs .group td span { font-weight: normal; color: #777; }
.booktabs .iv { color: #00a040; font-weight: bold; }
.booktabs-wrap { overflow-x: auto; }
</style>

<h1 style="text-align: center;">S2MDF: A Plug-And-Play Layer for Intersection-Free Multi-Object Signed Distance Fields</h1>
<h2 style="text-align: center;">Paper accepted to NeurIPS 2026</h2>

<h2 style="text-align: center;">
    <a class="page-link" href="https://scholar.google.com/citations?user=kpTb5N8AAAAJ&hl=en">Deniz Sayin Mercadier</a>*,
    <a class="page-link" href="https://scholar.google.com/citations?user=UxEI4sQAAAAJ&hl=en">Federico Stella</a>*,
    Aurel Bizeau,
    <a class="page-link" href="https://scholar.google.com/citations?hl=en&user=f2LbcbAAAAAJ">Nicolas Talabot</a>,
    <a class="page-link" href="https://scholar.google.com/citations?user=kzFmAkYAAAAJ&hl=en">Pascal Fua</a>
</h2>
<p style="text-align: center; color: #777; margin-top: -10px;">* equal contribution</p>

<div class="centered_div big">
    <div class="div_sidebyside"><img src="/papers/nsdudf/assets/epfl_logo.png"></div>
    <div class="div_sidebyside">
    	<a class="page-link" href="https://www.epfl.ch/labs/cvlab/">
    		<img src="/papers/nsdudf/assets/cvlab_logo.png"></a></div>
</div>

<div class="centered_div big" style="padding-bottom:20px;">
    <div class="div_rounded_corners" style="width: 220px;"><a href="https://arxiv.org/abs/2605.29761" style="color: #fdfdfd;">
        <i class="ai ai-arxiv"></i> Paper + Supp (Arxiv)
    </a></div>
    <div class="div_rounded_corners" style="width: 220px;"><a href="https://youtu.be/Fm-X_E88Es8" style="color: #fdfdfd;">
        &#9654; Video (5 min)
    </a></div>
    <div class="div_rounded_corners" style="width: 220px;"><a style="color: #fdfdfd;">
        <i class="ai ai-arxiv"></i> Poster - Coming Soon
    </a></div>
    <div class="div_rounded_corners" style="width: 220px;"><p style="color: #fdfdfd;"><object data="/assets/github_logo.svg"></object>
        <a style="color: #fdfdfd;">Code - Coming Soon</a>
    </p></div>
</div>

<h2 style="text-align: center;"> Feel free to contact us for any questions! </h2>

<h1 style="text-align: center;">S2MDF at a glance</h1>
<video class="s2mdf-video" src="/papers/s2mdf/assets/explainer.mp4" autoplay muted loop playsinline controls disablepictureinpicture controlslist="nodownload noplaybackrate"></video>
<div class="div_abstract">
	Each object of a compositional scene has its own Signed Distance Field (SDF), so nothing prevents two objects from interpenetrating. We require the two smallest SDF values at every point to sum to a non-negative number: the <b>MDF constraint</b>, which rules out intersections (Theorem 1). S2MDF enforces it in closed form by shifting all SDFs together (Shift-All), and since linear interpolation preserves the constraint (Theorem 2), standard Marching Cubes / Tetrahedra produce intersection-free meshes.
</div>

<div class="div_abstract">
	<h1 style="text-align: center;">Abstract</h1>
	Compositional implicit surface representations model scenes as collections of objects, each encoded by a Signed Distance Field (SDF). A fundamental limitation of this approach is that multiple SDFs can produce geometries that interpenetrate, violating physical plausibility. Existing mitigation strategies rely on soft penalty terms that reduce but do not eliminate intersections, and require careful loss weighting. To truly prevent interpenetration, we propose a hard constraint on vector-valued SDFs and introduce S2MDF, a lightweight plug-and-play module that enforces the constraint on any object-compositional SDF representation without architectural modifications. It introduces negligible computational overhead and is compatible with linearly-interpolated standard meshing algorithms such as Marching Cubes. It can be applied during training or as a post-processing step. Experiments on multiple state-of-the-art compositional methods show that S2MDF reduces intersections to numerical precision while preserving reconstruction quality, outperforming existing mitigation strategies.
</div>

<h1 style="text-align: center;">Presentation</h1>
<div class="auto-resizable-iframe">
  <div>
    <iframe src="https://www.youtube-nocookie.com/embed/Fm-X_E88Es8" title="S2MDF presentation (NeurIPS 2026)" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  </div>
</div>

<h1 style="text-align: center; margin-top: 30px;">A plug-and-play layer</h1>
<div style="width: 100%; display:block; margin:auto; padding-bottom:2px;"><img style="margin:5px 0; border-radius:10px;" src="/papers/s2mdf/assets/architecture.png" alt="p goes through a multi-object SDF network, giving SDF(p); the S2MDF layer turns it into MDF(p)" /></div>
<div class="div_abstract">
	S2MDF sits on top of any network that predicts one SDF per object, without changing its architecture. It acts point-wise, adds no parameters and only a negligible cost, and can be used while training or as post-processing on an already-trained model.
</div>

<h1 style="text-align: center;">Results</h1>
<div class="s2mdf-results">
	<div class="div_abstract" style="margin-top: 0; padding-top: 0;">
		We plug S2MDF into three state-of-the-art compositional methods: ObjectSDF++ (indoor scenes), PartSDF (part-based shapes) and MedTet (medical shapes). Each video zooms in and then shows the objects in transparency: <b>red</b> regions are intersections between objects, <b>green</b> regions are contacts without interpenetration.
	</div>
	<div class="s2mdf-labels"><div>Vanilla</div><div>S2MDF Shift-All (PP)</div><div>S2MDF Shift-All (Train)</div></div>

	<h3>ObjectSDF++</h3>
	<div class="note">Replica room 0, 256&#xB3; grid. (Train) uses the skip-connection variant.</div>
	<video class="s2mdf-video" src="/papers/s2mdf/assets/compare_scene.mp4" autoplay muted loop playsinline controls disablepictureinpicture controlslist="nodownload noplaybackrate"></video>

	<h3>PartSDF</h3>
	<div class="note">PartNet chairs, 128&#xB3; grid.</div>
	<video class="s2mdf-video" src="/papers/s2mdf/assets/compare_chair.mp4" autoplay muted loop playsinline controls disablepictureinpicture controlslist="nodownload noplaybackrate"></video>

	<h3>MedTet</h3>
	<div class="note">MM-WHS heart, 64&#xB3; tetrahedral grid subdivided once.</div>
	<video class="s2mdf-video" src="/papers/s2mdf/assets/compare_heart.mp4" autoplay muted loop playsinline controls disablepictureinpicture controlslist="nodownload noplaybackrate"></video>
	<div class="s2mdf-legend"><span style="background:#f03030;"></span>intersection<span style="background:#30d040;"></span>contact</div>
	<div class="note" style="text-align:center;">PP: post-processing of the trained vanilla model. Train: S2MDF used during training.</div>
</div>

<h1 style="text-align: center; margin-top: 30px;">Quantitative results</h1>
<div class="booktabs-wrap">
<table class="booktabs">
  <thead>
    <tr><th></th><th>MCD &#x2193;</th><th>MNC &#x2191;</th><th>F1 &#x2191;</th><th>IoU &#x2191;</th><th>IV &#x2193;</th></tr>
  </thead>
  <tbody>
    <tr class="group"><td colspan="6">ObjectSDF++ <span>&#xB7; Replica, 8 scenes &#xB7; MCD &#xD7;10&#x207B;&#xB2;</span></td></tr>
    <tr><td>Vanilla ObjectSDF++</td><td>10.677</td><td>77.953</td><td>66.946</td><td>&#x2013;</td><td>1.4&#xB7;10&#x207B;&#xB3;</td></tr>
    <tr><td>S2MDF Shift-All (PP)</td><td>3.345</td><td>78.058</td><td>68.325</td><td>&#x2013;</td><td class="iv">1.3&#xB7;10&#x207B;&#x2077;</td></tr>
    <tr><td>S2MDF Shift-All (Train)*</td><td>3.942</td><td>78.430</td><td>68.623</td><td>&#x2013;</td><td class="iv">1.5&#xB7;10&#x207B;&#x2076;</td></tr>
    <tr class="group"><td colspan="6">PartSDF <span>&#xB7; PartNet chairs &#xB7; MCD &#xD7;10&#x207B;&#x2074;</span></td></tr>
    <tr><td>Vanilla PartSDF</td><td>4.331</td><td>95.119</td><td>96.731</td><td>85.630</td><td>1.9&#xB7;10&#x207B;&#xB3;</td></tr>
    <tr><td>S2MDF Shift-All (PP)</td><td>1.973</td><td>94.824</td><td>98.005</td><td>89.173</td><td class="iv">5.2&#xB7;10&#x207B;&#x2079;</td></tr>
    <tr><td>S2MDF Shift-All (Train)</td><td>2.120</td><td>94.823</td><td>98.039</td><td>89.297</td><td class="iv">5.7&#xB7;10&#x207B;&#x2079;</td></tr>
    <tr class="group"><td colspan="6">MedTet <span>&#xB7; MM-WHS heart &#xB7; MCD &#xD7;10&#x207B;&#x2074;</span></td></tr>
    <tr><td>Vanilla MedTet</td><td>23.863</td><td>94.333</td><td>97.470</td><td>83.580</td><td>3.4&#xB7;10&#x207B;&#x2074;</td></tr>
    <tr><td>S2MDF Shift-All (PP)</td><td>31.099</td><td>94.316</td><td>97.297</td><td>83.694</td><td class="iv">9.9&#xB7;10&#x207B;&#xB9;&#xB2;</td></tr>
    <tr><td>S2MDF Shift-All (Train)</td><td>23.094</td><td>94.407</td><td>97.556</td><td>83.901</td><td class="iv">4.6&#xB7;10&#x207B;&#xB9;&#xB9;</td></tr>
  </tbody>
</table>
</div>
<div class="div_abstract" style="margin-top: 0;">
	Same reconstruction quality, with the <b>intersection volume (IV) down to numerical precision</b>. MCD: mean Chamfer distance, MNC: mean normal consistency, IV: intersection volume. *Skip-connection variant. Mean over 3 runs. See the paper for comparisons with existing mitigation strategies.
</div>

<h2> BibTeX </h2>
If you find our work useful, please cite it:

{% raw %}<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>@inproceedings{sayinmercadierstella2026s2mdf,
  author    = {Sayin Mercadier, Deniz and Stella, Federico and Bizeau, Aurel and Talabot, Nicolas and Fua, Pascal},
  title     = {{S2MDF}: A Plug-And-Play Layer for Intersection-Free Multi-Object Signed Distance Fields},
  booktitle = {Advances in Neural Information Processing Systems},
  year      = {2026}
}
</code></pre></div></div>{% endraw %}
