---
layout: index
title: Hyspecnet
permalink: /
---

## About HySpecNet-11K

The HySpecNet-11K dataset is constructed by the <a href="https://rsim.berlin" target="_blank">Remote Sensing Image Analysis (RSiM)</a> group at <a href="https://tu.berlin" target="_blank">TU Berlin</a> and the Big Data Analytics in Earth Observation group at the <a href="https://bifold.berlin" target="_blank">Berlin Institute for the Foundations of Learning and Data (BIFOLD)</a>.

HySpecNet-11K is a large-scale hyperspectral benchmark dataset made up of 11,483 nonoverlapping image patches acquired by the <a href="https://www.enmap.org" target="_blank">EnMAP satellite</a>. Each patch is a portion of 128 × 128 pixels with 224 spectral bands and with a ground sample distance of 30 m.

<p class="lead">
<i class="fas fa-info-circle hyspec"></i>
To construct HySpecNet-11K, a total of 250 EnMAP tiles acquired during the routine operation phase between 2 November 2022 and 9 November 2022 were considered. The considered tiles are associated with less than 10% cloud and snow cover. The tiles were radiometrically, geometrically and atmospherically corrected (L2A water & land product). Then, the tiles were divided into nonoverlapping image patches. The cropped patches at the borders of the tiles were eliminated. As a result,  more than 45 patches per tile are obtained, resulting in 11,483 patches for the full dataset.
</p>
<p class="lead">
<i class="fas fa-info-circle hyspec"></i>
We provide predefined splits obtained by randomly dividing HySpecNet into: i) a training set that includes 70% of the patches, ii) a validation set that includes 20% of the patches, and iii) a test set that includes 10% of the patches. Depending on the way that we used for splitting the dataset, we define two different splits: i) an easy split, where patches from the same tile can be present in different sets (patchwise splitting); and ii) a hard split, where all patches from one tile belong to the same set (tilewise splitting).
</p>

For further details about HySpecNet-11K, please see our paper:

<blockquote>
    M. H. P. Fuchs and B. Demіr, "<a href="https://arxiv.org/abs/2306.00385">HySpecNet-11K: A Large-Scale Hyperspectral Dataset for Benchmarking Learning-Based Hyperspectral Image Compression Methods</a>", IEEE International Geoscience and Remote Sensing Symposium, Pasadena, California, 2023.
</blockquote>

<section class="download">
    <h2 id="downloads">Downloads</h2>
    <p>
    If you use HySpecNet-11K in your research, please cite our paper:
    </p>
    <blockquote>
        M. H. P. Fuchs and B. Demіr, "<a href="https://arxiv.org/abs/2306.00385">HySpecNet-11K: A Large-Scale Hyperspectral Dataset for Benchmarking Learning-Based Hyperspectral Image Compression Methods</a>", IEEE International Geoscience and Remote Sensing Symposium, Pasadena, California, 2023.
    </blockquote>
    <div class="h-100 d-flex align-items-center justify-content-center">
        <div class="card downloads">
            <div class="card-header text-center">
                <h5 class="card-title">HySpecNet-11K</h5>
            </div>
            <div class="card-body">
            <!-- Grid -->
                <div class="row">
                    <div class="col-lg-6 col-md-4 col-sm2">
                        <p class="card-text">
                            <i class="fas fa-download mb-2"></i>
                            <a href="https://hyspecnet.rsim.berlin">HySpecNet-11K Download</a>
                        </p>
                    </div>
                    <div class="col-lg-6 col-md-4 col-sm2">
                        <p class="card-text">
                            <i class="fas fa-newspaper  mb-2"></i>
                            <a href="{{ site.url }}/hyspecnet-11k-description/">HySpecNet-11K Description</a>
                        </p>
                    </div>
                </div>
                <div class="row">
                    <div class="col-lg-6 col-md-4 col-sm2">
                        <p class="card-text">
                            <i class="fas fa-tools  mb-2"></i>
                            <a href="https://git.tu-berlin.de/rsim/hyspecnet-tools" target="_blank">HySpecNet Tools</a>
                        </p>
                    </div>
                    <div class="col-lg-6 col-md-4 col-sm2">
                        <p class="card-text">
                            <i class="fab fa-gitlab  mb-2"></i>
                            <a href="https://git.tu-berlin.de/rsim/hsi-compression">Deep Learning Models</a>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>

</section>

<section class="faq">
    <h2 id="faq">FAQ</h2>
    <div class="accordion" id="accordionExample">
        <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
            <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
                How do I unpack the &quot;hyspecnet-11k.tar.gz&quot; file?
            </button>
            </h2>
            <div id="collapseOne" class="accordion-collapse collapse" aria-labelledby="headingOne" data-bs-parent="#accordionExample">
            <div class="accordion-body">
                To unpack the <code class="language-bash">hyspecnet-11k.tar.gz</code> tarball use the following command:
                <pre><code class="language-bash">tar -xzf hyspecnet-11k.tar.gz</code></pre>
            </div>
            </div>
        </div>
        <div class="accordion-item">
            <h2 class="accordion-header" id="headingTwo">
            <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                Where are the preprocessed &quot;*-DATA.npy&quot; files?
            </button>
            </h2>
            <div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo" data-bs-parent="#accordionExample">
            <div class="accordion-body">
                The <code class="language-bash">*-DATA.npy</code> files have to be generated by running the <a href="https://git.tu-berlin.de/rsim/hyspecnet-tools/-/blob/main/tif_to_npy.ipynb" target="_blank">tif_to_npy.ipynb</a> notebook from the <a href="https://git.tu-berlin.de/rsim/hyspecnet-tools" target="_blank">HySpecNet Tools</a>.
            </div>
            </div>
        </div>
        <div class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
            <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                Is there any hyperspectral image band affected by the strong water vapor absorption in this dataset?
            </button>
            </h2>
            <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree" data-bs-parent="#accordionExample">
            <div class="accordion-body">
                The bands [127 – 141] and [161 – 167] are affected by strong water vapor absorption and suggested not to be considered for the training of the deep learning models.
            </div>
            </div>
        </div>
    </div>

</section>

<section class="license text-center" id="license">
    The HySpecNet-11K dataset is licensed under <a href="https://creativecommons.org/publicdomain/zero/1.0/" >CC0 1.0 Universal (CC0 1.0)
Public Domain Dedication</a>.
</section>
