---
layout: paper
title: "HRUDF"
permalink: /hrudf/
description: High Resolution UDF Meshing via Iterative Networks
---

<!-- Import 3D viewer component -->
<script type="module" src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js"></script>

<h1 style="text-align: center;">High Resolution UDF Meshing via Iterative Networks</h1>
<h2 style="text-align: center;">Paper accepted to NeurIPS 2025</h2>

<h2 style="text-align: center;">
    <a class="page-link" href="https://scholar.google.com/citations?user=UxEI4sQAAAAJ&hl=en">Federico Stella</a>,
    <a class="page-link" href="https://scholar.google.com/citations?hl=en&user=f2LbcbAAAAAJ">Nicolas Talabot</a>,
    <a class="page-link" href="https://scholar.google.com/citations?hl=en&user=Bj9g-EEAAAAJ">Hieu Le</a>,
    <a class="page-link" href="https://scholar.google.com/citations?user=kzFmAkYAAAAJ&hl=en">Pascal Fua</a>
</h2>


<div class="centered_div big">
    <div class="div_sidebyside"><img src="/papers/nsdudf/assets/epfl_logo.png"></div>
    <div class="div_sidebyside">
    	<a class="page-link" href="https://www.epfl.ch/labs/cvlab/">
    		<img src="/papers/nsdudf/assets/cvlab_logo.png"></a></div>
</div>

<div class="centered_div big" style="padding-bottom:20px;">
    <div class="div_rounded_corners" style="width: 220px;"><a href="https://arxiv.org/abs/2509.17212" style="color: #fdfdfd;">
        <i class="ai ai-arxiv"></i> Paper + Supp (Arxiv)
    </a></div>
    <div class="div_rounded_corners" style="width: 220px;"><a href="/papers/hrudf/assets/NeurIPS poster6.pdf" style="color: #fdfdfd;">
        <i class="ai ai-arxiv"></i> Poster (NeurIPS 2025)
    </a></div>
    <div class="div_rounded_corners" style="width: 220px;"><p style="color: #fdfdfd;"><object data="/assets/github_logo.svg"></object>
        <a style="color: #fdfdfd;">Code - Coming Soon</a>
    </p></div>
</div>

<h2 style="text-align: center;"> Feel free to contact us for any questions! </h2>

<div style="width: 100%; display:block; margin:auto; padding-bottom:2px;"><img style="margin:5px; border-radius:10px;" src="/papers/hrudf/assets/teaser_animation.gif" /></div>

<div class="div_abstract">
	<h1 style="text-align: center;">Abstract</h1>
	Unsigned Distance Fields (UDFs) are a natural implicit representation for open surfaces but, unlike Signed Distance Fields (SDFs), are challenging to triangulate into explicit meshes. This is especially true at high resolutions where neural UDFs exhibit higher noise levels, which makes it hard to capture fine details. Most current techniques perform within single voxels without reference to their neighborhood, resulting in missing surface and holes where the UDF is ambiguous or noisy. We show that this can be remedied by performing several passes and by reasoning on previously extracted surface elements to incorporate neighborhood information. Our key contribution is an iterative neural network that does this and progressively improves surface recovery within each voxel by spatially propagating information from increasingly distant neighbors. Unlike single-pass methods, our approach integrates newly detected surfaces, distance values, and gradients across multiple iterations, effectively correcting errors and stabilizing extraction in challenging regions. Experiments on diverse 3D models demonstrate that our method produces significantly more accurate and complete meshes than existing approaches, particularly for complex geometries, enabling UDF surface extraction at higher resolutions where traditional methods fail.
</div>

<h1 style="text-align: center;">The problem</h1>
<div style="width: 100%; display:block; margin:auto; padding-bottom:2px;"><img style="margin:5px; border-radius:10px;" src="/papers/hrudf/assets/resolution.png" /></div>
<div class="div_abstract">
	Neural UDFs are noisy and difficult to mesh. Counterintuitively, meshing at higher resolutions worsens the problem, with existing methods often missing entire portions of the surface.
</div>

<h1 style="text-align: center;">Our pipeline</h1>
<div style="width: 100%; display:block; margin:auto; padding-bottom:2px;"><img style="margin:5px; border-radius:10px;" src="/papers/hrudf/assets/pipeline.png" /></div>
<div class="div_abstract">
	We formulate high-resolution meshing as an iterative process: each iteration takes the previous output state as input and refines it.
</div>

<h1 style="text-align: center;">An iterative improvement</h1>
<div style="width: 100%; display:block; margin:auto; padding-bottom:2px;"><img style="margin:5px; border-radius:10px;" src="/papers/hrudf/assets/iterations.png" /></div>
<div class="div_abstract">
	The mesh is improved over multiple iterations, where each step integrates newly detected surfaces, distance values, and gradients from neighboring cells.
</div>

<h1 style="text-align: center;">The result</h1>
<div style="width: 100%; display:block; margin:auto; padding-bottom:2px;"><img style="margin:5px; border-radius:10px;" src="/papers/hrudf/assets/results.png" /></div>
<div class="div_abstract">
	While still being far from perfect, we obtain state of the art results across multiple datasets and with multiple different UDF backbones.
</div>


<h2> BibTeX </h2>
If you find our work useful, please cite it:

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>@misc{stella2025hrudf,
      title={High Resolution UDF Meshing via Iterative Networks}, 
      author={Federico Stella and Nicolas Talabot and Hieu Le and Pascal Fua},
      year={2025},
      eprint={2509.17212},
      archivePrefix={arXiv},
      primaryClass={cs.GR},
      url={https://arxiv.org/abs/2509.17212}, 
}
</code></pre></div></div>

<!-- 
<hr class="hr_style">

<div class="div_text div_gray">
  <h3> Example </h3>

<table >
<tr>
<td>
	<div class="auto-resizable-mv">
  	<div>
  		<model-viewer interpolation-decay="0" alt="Inflated" src="/projects/meshudf/meshes/pants_inflated2.glb" shadow-intensity="1" poster="/projects/meshudf/meshes/pants_inflated2.png"  orientation="0deg -30deg 0deg" field-of-view="39deg" camera-controls touch-action="pan-y"></model-viewer>
  	</div></div>
</td>
<td>
	<div class="auto-resizable-mv">
  	<div>
  		<model-viewer alt="BP" src="/projects/meshudf/meshes/pants_bp2.glb" shadow-intensity="1" poster="/projects/meshudf/meshes/pants_bp2.png"  orientation="0deg -30deg 0deg" field-of-view="39deg" camera-controls touch-action="pan-y"></model-viewer></div></div>
</td>
<td>
	<div class="auto-resizable-mv">
  	<div>
	<model-viewer interpolation-decay="0" alt="Ours" src="/projects/meshudf/meshes/pants_ours2.glb" poster="/projects/meshudf/meshes/pants_ours2.png" shadow-intensity="1"  orientation="0deg -30deg 0deg" field-of-view="39deg" camera-controls touch-action="pan-y"></model-viewer>
	</div></div>
</td>
</tr>
<tr>

<td><center><small><b>(a)</b><i> [<i>MC</i>] on an ε>0 level set </i></small></center></td>
<td><center><small><b>(b)</b><i> Meshing a point cloud </i></small></center></td>
<td><center><small><b>(c)</b><i> Our procedure </i></small></center></td>
</tr>
</table>


  <div style="width: 100%; display:inline-block;">
    
The UDF of a pair of trousers is meshed by either <b>(a)</b> Marching Cubes [<i>MC</i>] on the ε>0 level set, <b>(b)</b> meshing a dense point cloud as in [<i>NDF</i>], or <b>(c)</b>  our algorithm.
<br>
Using <b>(a)</b>, the shape is inflated and artificially thickened (visible at the leg openings). With <b>(b)</b>, the mesh is open but rough, and the procedure is slow. In contrast, our method <b>(c)</b> quickly obtains an open and regular mesh.

  </div>
</div>


<div class="div_text div_gray">
	<h3> Approach </h3>
  <div class="div_aligned">
    <div class="split_img_if_possible right" ><img style="margin:5px; width:100%;border-radius:10px;" src="/projects/meshudf/images/method.png" /> 
    </div>
    <div class="split_text_if_possible" >
      UDFs do not have sign flips, thus Marching Cubes [<i>MC</i>] does not apply directly. Instead, at each grid cell we rely on gradient orientations to infer local pseudo-signs. To ensure consistency between the pseudo-signs of neighboring grid cells, we explore the grid in a breadth-first manner.
    </div>
  </div>
</div>




<div class="div_text div_gray">
  <h3> Differentiability </h3>
  <div class="div_aligned">
  <div class="split_text_if_possible" >
    When the UDF <i>φ(.)</i> is decoded by a network from a latent code <b>z</b>, we provide gradients for mesh vertices <b>v</b> w.r.t. <b>z</b>.
    Since <b>v</b> lies at a singularity of the field, we control the <b>α>0</b> level sets using differentiability results from [<i>MS</i>]. Intuitively, when the UDF increases at <b>v<sub>-</sub></b> and decreases at <b>v<sub>+</sub></b>, <b>v</b> moves in the direction of the normal <b>n</b>.
  </div>
  <div class="split_img_if_possible left"><img style="margin:5px; border-radius:10px;" src="/projects/meshudf/images/gradients.png" /></div>
  </div>
</div>

<div class="div_text div_gray">
  <h3> Optimization </h3>
    With the above gradients, a frozen UDF decoder can be used as a differentiable parameterization of open surface meshes. In this example, we start from the latent code of a pair of trousers, and optimize it so that the corresponding output mesh matches the silhouette of a tshirt. 
    <br>Using our gradients and a differentiable rasterizer of meshes, we simply minimize a pixel space loss via gradient descent. The latent space traversal eventually results in a topology change.
    <div style="width: 100%; display:block; margin:auto; padding-bottom:2px;"><img style="margin:5px; border-radius:10px;" src="/projects/meshudf/images/silh_optim.gif" /></div>
  	<div style="width: 100%; display:inline-block;">
  </div>
</div>

<h2> BibTeX </h2>
If you find our work useful, please cite it:

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>@inproceedings{guillard2022udf,
  author = {Guillard, Benoit and Stella, Federico and Fua, Pascal},
  title = {MeshUDF: Fast and Differentiable Meshing of Unsigned Distance Field Networks},
  booktitle = {European Conference on Computer Vision},
  year = {2022}
}
</code></pre></div></div>


<hr class="hr_style_thin">

<h3> References </h3>


<div class="div_refs">
  <div class="div_aligned_top">
    <div style="width: 12%; display:inline-block; text-align:right; margin-right:1%;">[<i>MC</i>]</div>
    <div style="width: 87%; display:inline-block;">Marching Cubes: a High Resolution 3D Surface Construction Algorithm, Lorensen and Cline, <i>SIGGRAPH</i> 1987.</div>
  </div>
</div>
<div class="div_refs">
  <div class="div_aligned_top">
    <div style="width: 12%; display:inline-block; text-align:right; margin-right:1%;">[<i>NDF</i>]</div>
    <div style="width: 87%; display:inline-block;">Neural Unsigned Distance Fields for Implicit Function Learning, Chibane et al., <i>NeurIPS</i> 2020.</div>
  </div>
</div>
<div class="div_refs">
  <div class="div_aligned_top">
    <div style="width: 12%; display:inline-block; text-align:right; margin-right:1%;">[<i>MS</i>]</div>
    <div style="width: 87%; display:inline-block;">MeshSDF: Differentiable Iso-Surface Extraction, Remelli et al., <i>NeurIPS</i> 2020.</div>
  </div>
</div> -->