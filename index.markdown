---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<style>
/* Split the screen in half */
.split {
    display: block;
    height: 100%;
    width: 50%;
  }
  
  /* Control the left side */
.left {
    float:left;
    margin:5px; 
}
  
/* Control the right side */
.right {
    float:right;
    margin:5px; 
}

.small {
	/* width: 26%;  */
	width: 26%;
}

.big {
	width: 68%;
}

</style>


<div>
    <div class="split right" style="width: 40%">
        <div>
        <img id="pp" src="/assets/3B8A0921.jpg" />
        </div>
    </div>
    <div class="split left" style="text-align: justify; text-justify: inter-word;">
    	<h1>Hello!</h1>
        <p>I am Federico, a PhD student at <b><a href="https://www.epfl.ch/"> EPFL</a></b> in Lausanne, Switzerland. I work on 3D Computer Vision in <b><a href="http://cvlab.epfl.ch">EPFL’s CVLab</a></b>, supervised by <b><a href="https://scholar.google.com/citations?user=kzFmAkYAAAAJ&hl=en&oi=ao">Prof. Pascal Fua</a></b>. My research lies mainly on neural implicit representations for 3D surfaces, with a particular interest in surfaces with difficult topologies, represented using Unsigned Distance Fields. Neural representations are quite fun in general, so I'm also working on image compression using them.</p>
        A part from research, I love beach tennis (as clear from the pic on the right), bouldering, photography, and I play a bit of music (guitar, drums, sing). If you want to see my research, it's below; if you want to see my pics and music, here's my <a href="https://www.youtube.com/@federicostella95">YouTube</a> and <a href="https://www.instagram.com/ilceltico/">Instagram</a> :)
    </div>
</div>

<div style="clear: both;"> </div>


# Publications
*(full list on [scholar](https://scholar.google.com/citations?user=UxEI4sQAAAAJ&hl=en))*

<div>
    <div class="split left small">
        <div>
            <video width="100%" muted autoplay>
                <source src="/assets/ours.mp4" type="video/mp4">
            </video>
        </div>
    </div>
    <div class="split right big">
    	<h2>Neural Surface Detection for Unsigned Distance Fields</h2>
        <p><a class="page-link" href="https://scholar.google.com/citations?user=UxEI4sQAAAAJ&hl=en">Federico Stella</a>,
        <a class="page-link" href="https://scholar.google.com/citations?hl=en&user=f2LbcbAAAAAJ">Nicolas Talabot</a>,
        <a class="page-link" href="https://scholar.google.com/citations?hl=en&user=Bj9g-EEAAAAJ">Hieu Le</a>,
        <a class="page-link" href="https://scholar.google.com/citations?user=kzFmAkYAAAAJ&hl=en">Pascal Fua</a>; at ECCV 2024 </p>
        <p><b>
            <a href="/nsdudf">[Project Page]</a>
        	<a href="https://arxiv.org/abs/2407.18381">[Paper]</a>
        	<a href="https://github.com/ilceltico/nsdudf">[Code]</a>
        </b></p>
        <p>A neural approach to turn a UDF into a local SDF, which can be meshed with traditional algorithms.</p>
    </div>
</div>

<div style="clear: both;"> </div>


<div>
    <div class="split left small">
        <div>
        <img id="pp" src="/assets/meshudf.gif" />
        </div>
    </div>
    <div class="split right big">
    	<h2>MeshUDF: Fast and Differentiable Meshing of Unsigned Distance Field Networks</h2>
        <p><a href="https://scholar.google.com/citations?user=9c5ruhsAAAAJ&hl=en&oi=ao">Benoit Guillard</a>,
        <a href="https://scholar.google.com/citations?user=UxEI4sQAAAAJ&hl=en&oi=ao">Federico Stella</a>,
        <a href="https://scholar.google.com/citations?user=kzFmAkYAAAAJ&hl=en&oi=ao">Pascal Fua</a>; at ECCV 2022</p>
        <p><b>
        	<a href="https://bguillard.github.io/meshudf/">[Project Page]</a>
        	<a href="https://arxiv.org/abs/2111.14549">[Paper]</a>
        	<a href="https://github.com/cvlab-epfl/MeshUDF">[Code]</a>
        </b></p>
        <p>An extension of Marching Cubes to mesh non-watertight surfaces, applied the output of Unsigned Distance Field networks. We also derive gradients for the reconstructed vertex positions wrt. the UDF field.</p>
    </div>
</div>

<div style="clear: both;"> </div>

<div>
    <div class="split left small">
        <div>
        <img id="pp" src="/assets/compass.png" />
        </div>
    </div>
    <div class="split right big">
    	<h2>Compass: Learning to Orient Surfaces by Self-supervised Spherical CNNs</h2>
        <p><a href="https://scholar.google.com/citations?user=DYADxJAAAAAJ&hl=en&oi=ao">Riccardo Spezialetti</a>,
        <a href="https://scholar.google.com/citations?user=UxEI4sQAAAAJ&hl=en">Federico Stella</a>,
        <a href="https://scholar.google.com/citations?user=JfR9nm0AAAAJ&hl=en&oi=ao">Marlon Marcon</a>,
        <a href="https://scholar.google.com/citations?user=_xB5NUgAAAAJ&hl=en">Luciano Silva</a>,
        <a href="https://scholar.google.com/citations?user=1kcIJG0AAAAJ&hl=en">Samuele Salti</a>,
        <a href="https://scholar.google.com/citations?user=xZVTzyAAAAAJ&hl=en">Luigi Di Stefano</a>; at NeurIPS 2020</p>
        <p><b>
        	<a href="https://arxiv.org/abs/2011.03298">[Paper]</a>
        	<a href="https://github.com/CVLAB-Unibo/compass">[Code]</a>
        </b></p>
        <p>The first end-to-end trained Local Reference Frame for point clouds. It employs Spherical CNNs to extract rotation-invariant features from point clouds, and uses them to locally orient surface patches in a canonical way.</p>
    </div>
</div>

<div style="clear: both;"> </div>