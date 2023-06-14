---
layout: index
title: Hyspecnet
permalink: /
---

<section class="patches justify-items-center">
    <div class="row">
    {% for i in (1..20) %}
        <div class="col m-0 p-0">
            <img src="{{ site.url }}/../assets/images/thumbnails/{{ i }}.jpg">
        </div>
    {% endfor %}
    </div>
</section>

<section class="logos">
    <div class="row">
        <div class="col">
            <div class="text-center mx-auto mb-5 mb-lg-0 mb-lg-3">
                <a href="https://www.tu-berlin.de" target="_blank">
                    <img src="assets/images/tu-logo.svg" class="img-responsive center-block" style="height: 50px">
                </a>
            </div>
        </div>
        <div class="col">
            <div class="text-center mx-auto mb-5 mb-lg-0 mb-lg-3">
                <a href="http://bifold.berlin" target="_blank">
                    <img src="assets/images/BIFOLD.svg" class="img-responsive center-block" style="height: 50px">
                </a>
            </div>
        </div>
        <div class="col">
            <div class="text-center mx-auto mb-5 mb-lg-0 mb-lg-3">
                <a href="https://rsim.berlin" target="_blank">
                    <img src="assets/images/rsim-logo.png" class="img-responsive center-block" style="height: 50px">
                </a>
            </div>
        </div>
        <div class="col">
            <div class="text-center mx-auto mb-5 mb-lg-0 mb-lg-3">
                <a href="http://www.bigearth.eu" target="_blank">
                    <img src="assets/images/BigEarth.png" class="img-responsive center-block" style="height: 50px">
                </a>
            </div>
        </div>
    </div>
</section>

## About HySpecNet-11K

The HySpecNet-11K dataset is constructed by the <a href="https://rsim.berlin" target="_blank">Remote Sensing Image Analysis (RSiM)</a> group at <a href="https://tu.berlin" target="_blank">TU Berlin</a> and the Big Data Analytics in Earth Observation group at the <a href="https://bifold.berlin" target="_blank">Berlin Institute for the Foundations of Learning and Data (BIFOLD)</a>.

HySpecNet-11K is a large-scale hyperspectral benchmark dataset made up of 11,483 nonoverlapping image patches acquired by the <a href="https://www.enmap.org" target="_blank">EnMAP satellite</a>. Each patch is a portion of 128 × 128 pixels with 224 spectral bands and with a ground sample distance of 30 m.

<div class="card">
  <div class="card-body">
    <p class="card-text">To construct HySpecNet-11K, a total of 250 EnMAP tiles acquired during the routine operation phase between 2 November 2022 and 9 November 2022 were considered. The considered tiles are associated with less than 10% cloud and snow cover. The tiles were radiometrically, geometrically and atmospherically corrected (L2A water & land product). Then, the tiles were divided into nonoverlapping image patches. The cropped patches at the borders of the tiles were eliminated. As a result,  more than 45 patches per tile are obtained, resulting in 11,483 patches for the full dataset. Due to the L2A-processed data, the number of bands is reduced from 224 to 202 by removing bands [127 – 141] and [161 – 167] that are affected by strong water vapor absorption.
    </p>
    <p class="card-text">
    We provide predefined splits obtained by randomly dividing HySpecNet into: i) a training set that includes 70% of the patches, ii) a validation set that includes 20% of the patches, and iii) a test set that includes 10% of the patches. Depending on the way that we used for splitting the dataset, we define two different splits: i) an easy split, where patches from the same tile can be present in different sets (patchwise splitting); and ii) a hard split, where all patches from one tile belong to the same set (tilewise splitting).
    </p>
  </div>
</div>

For further details about HySpecNet-11K, please see our paper:

<blockquote>
    M. H. P. Fuchs and B. Demіr, "<a href="https://arxiv.org/abs/2306.00385">HySpecNet-11K: A Large-Scale Hyperspectral Dataset for Benchmarking Learning-Based Hyperspectral Image Compression Methods</a>", IEEE International Geoscience and Remote Sensing Symposium, Pasadena, California, 2023.
</blockquote>

# Downloads

If you use HySpecNet-11K in your research, please cite our paper:

<blockquote>
    M. H. P. Fuchs and B. Demіr, "<a href="https://arxiv.org/abs/2306.00385">HySpecNet-11K: A Large-Scale Hyperspectral Dataset for Benchmarking Learning-Based Hyperspectral Image Compression Methods</a>", IEEE International Geoscience and Remote Sensing Symposium, Pasadena, California, 2023.
</blockquote>

<div class="card" style="width:40%">
    <div class="card-header">
        <h5 class="card-title">HySpecNet-11K</h5>
    </div>
    <div class="card-body">
        <p class="card-text">
            <i class="fas fa-download font-color-ben mb-2"></i>
            Download <a href="https://hyspecnet.rsim.berlin/link-to-downloads/">Patches (tif) (~XX GB)</a>
        </p>
        <p class="card-text">
            <i class="fas fa-download font-color-ben mb-2"></i>
            Download <a href="https://hyspecnet.rsim.berlin/link-to-downloads/">Patches (numpy) (~XXX GB)</a>
        </p>
        <p class="card-text">
            <i class="fas fa-download font-color-ben mb-2"></i>
            Download <a href="https://hyspecnet.rsim.berlin/link-to-downloads/">Splits (~XXX kB)</a>
        </p>
        <p class="card-text">
            <i class="fas fa-download font-color-ben mb-2"></i>
            Download <a href="https://hyspecnet.rsim.berlin/link-to-downloads/">Thumbnails (~XX MB)</a>
        </p>
        <p class="card-text">
            <i class="fas fa-download font-color-ben mb-2"></i>
            Download <a href="https://hyspecnet.rsim.berlin/link-to-downloads/">Masks (tif) (~XX GB)</a>
        </p>
        <p class="card-text">
            <i class="fas fa-download font-color-ben mb-2"></i>
            Download <a href="https://hyspecnet.rsim.berlin/link-to-downloads/">Metadata (~XX MB)</a>
        </p>
        <p class="card-text">
            <i class="fas fa-download font-color-ben mb-2"></i>
            Download <a href="https://hyspecnet.rsim.berlin/link-to-downloads/hyspecnet-11k-description.pdf">Dataset Description</a>
        </p>
        <p class="card-text">
            <i class="fab fa-gitlab font-color-ben mb-2"></i>
            <a href="https://git.tu-berlin.de/rsim/hsi-compression">Deep Learning Models</a>
        </p>
        <p class="card-text">
            <i class="fas fa-tools font-color-ben mb-2"></i>
            <a href="https://git.tu-berlin.de/rsim/hyspecnet-11k-tools">Tools</a>
        </p>
    </div>
</div>

# FAQ

To be added.

<section class="license text-center">
    The HySpecNet-11K dataset is licensed under <a href="/downloads/documents/license.pdf" download="">the Community Data License Agreement – Permissive, Version 1.0</a>.
</section>
