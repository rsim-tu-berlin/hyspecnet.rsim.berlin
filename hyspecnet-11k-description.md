---
layout: index
title: Hyspecnet
permalink: /hyspecnet-11k-description/
---

# HySpecNet-11k Description

The HySpecNet-11k dataset is constructed by the [Remote Sensing Image Analysis (RSiM)](https://rsim.berlin) group at [TU Berlin](https://tu.berlin) and the Big Data Analytics in Earth Observation group at the [Berlin Institute for the Foundations of Learning and Data (BIFOLD)](https://bifold.berlin).

HySpecNet-11k is a large-scale hyperspectral benchmark dataset made up of 11,483 nonoverlapping image patches acquired by the [EnMAP satellite](https://www.enmap.org). Each patch is a portion of 128 × 128 pixels with 224 spectral bands and with a ground sample distance of 30 m.

To construct HySpecNet-11k, a total of 250 EnMAP tiles acquired during the routine operation phase between 2 November 2022 and 9 November 2022 were considered. The considered tiles are associated with less than 10% cloud and snow cover. The tiles were radiometrically, geometrically and atmospherically corrected (L2A water & land product). Then, the tiles were divided into nonoverlapping image patches. The cropped patches at the borders of the tiles were eliminated. As a result, more than 45 patches per tile are obtained, resulting in 11,483 patches for the full dataset.

We provide predefined splits obtained by randomly dividing HySpecNet into: i) a training set that includes 70% of the patches, ii) a validation set that includes 20% of the patches, and iii) a test set that includes 10% of the patches. Depending on the way that we used for splitting the dataset, we define two different splits: i) an easy split, where patches from the same tile can be present in different sets (patchwise splitting); and ii) a hard split, where all patches from one tile belong to the same set (tilewise splitting).

For further details about HySpecNet-11k, please see our paper:

> M. H. P. Fuchs and B. Demіr, "[HySpecNet-11k: A Large-Scale Hyperspectral Dataset for Benchmarking Learning-Based Hyperspectral Image Compression Methods](https://arxiv.org/abs/2306.00385)", IEEE International Geoscience and Remote Sensing Symposium, Pasadena, California, 2023.

The HySpecNet-11k dataset is licensed under a [CC0 1.0 Universal (CC0 1.0) Public Domain Dedication](https://creativecommons.org/publicdomain/zero/1.0/) license.

<div style="page-break-after: always;"></div>

## Folder Structure

The folder structure of the HySpecNet-11k dataset is as follows:

```
┗ 📂 hyspecnet-11k/
  ┣ 📂 patches/
  ┃ ┣ 📂 tile_001/
  ┃ ┃ ┣ 📂 tile_001-patch_01/
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-DATA.npy
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-QL_PIXELMASK.TIF
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-QL_QUALITY_CIRRUS.TIF
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-QL_QUALITY_CLASSES.TIF
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-QL_QUALITY_CLOUD.TIF
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-QL_QUALITY_CLOUDSHADOW.TIF
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-QL_QUALITY_HAZE.TIF
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-QL_QUALITY_SNOW.TIF
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-QL_QUALITY_TESTFLAGS.TIF
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-QL_SWIR.TIF
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-QL_VNIR.TIF
  ┃ ┃ ┃ ┣ 📜 tile_001-patch_01-SPECTRAL_IMAGE.TIF
  ┃ ┃ ┃ ┗ 📜 tile_001-patch_01-THUMBNAIL.jpg
  ┃ ┃ ┣ 📂 tile_001-patch_02/
  ┃ ┃ ┃ ┗ 📜 ...
  ┃ ┃ ┗ 📂 ...
  ┃ ┣ 📂 tile_002/
  ┃ ┃ ┗ 📂 ...
  ┃ ┗ 📂 ...
  ┗ 📂 splits/
    ┣ 📂 easy/
    ┃ ┣ 📜 test.csv
    ┃ ┣ 📜 train.csv
    ┃ ┗ 📜 val.csv
    ┣ 📂 hard/
    ┃ ┣ 📜 test.csv
    ┃ ┣ 📜 train.csv
    ┃ ┗ 📜 val.csv
    ┗ 📂 ...
```

There exists a folder for each tile, e.g.

```
hyspecnet-11k/patches/tile_001/
```

Inside this folder there are several subfolders with the patches belonging to that tile, e.g.

```
hyspecnet-11k/patches/tile_001/tile_001-patch_01/
```

Inside the patch folders are the files related to the patch, e.g.

```
hyspecnet-11k/patches/tile_001/tile_001-patch_01/tile_001-patch_01-SPECTRAL_IMAGE.TIF
```

## Naming Conventions

The folders and files described in previous section are stored with the following naming conventions (see [EnMAP HSI Level 1 / Level 2 Product Specification Document](https://www.enmap.org/data/doc/EN-PCV-ICD-2009-2_HSI_Product_Specification_Level1_Level2.pdf) for further details).

### Tile Folders

The compact naming convention for each tile product is defined as follows:

```
ENMAP01-<productType>-DT<datatakeID>_<timeStartDatatake>_<tileID>_<version>_<timeProcessing>Z-<file_name>/
```

### Patch Folders

The compact naming convention for each patch folder is defined as follows:

```
ENMAP01-<productType>-DT<datatakeID>_<timeStartDatatake>_<tileID>_<version>_<timeProcessing>Z-Y<yStart><yEnd>_X<xStart><xEnd>/
```

### Patch Product Files

The compact naming convention for each patch product is defined as follows:

```
ENMAP01-<productType>-DT<datatakeID>_<timeStartDatatake>_<tileID>_<version>_<timeProcessing>Z-Y<yStart><yEnd>_X<xStart><xEnd>-<file_name>.<extension>
```

The following products are available for each patch.

```
*-DATA.npy
*-QL_PIXELMASK.TIF
*-QL_QUALITY_CIRRUS.TIF
*-QL_QUALITY_CLASSES.TIF
*-QL_QUALITY_CLOUD.TIF
*-QL_QUALITY_CLOUDSHADOW.TIF
*-QL_QUALITY_HAZE.TIF
*-QL_QUALITY_SNOW.TIF
*-QL_QUALITY_TESTFLAGS.TIF
*-QL_SWIR.TIF
*-QL_VNIR.TIF
*-SPECTRAL_IMAGE.TIF
*-THUMBNAIL.jpg
```

## File Formats

### Hyperspectral Data

The hyperspectral data for each patch is stored in geotiff format (`*-SPECTRAL_IMAGE.TIF`).

### Preprocessed Numpy Files

The preprocessed hyperspectral data for each patch is stored in numpy format (`*-DATA.npy`).
To generate the preprocessed NumPy files, run the [tif_to_npy.ipynb](https://git.tu-berlin.de/rsim/hyspecnet-tools/-/blob/main/tif_to_npy.ipynb) notebook from the [HySpecNet Tools](https://git.tu-berlin.de/rsim/hyspecnet-tools).

### Thumbnails

For each patch there exists a thumbnail (`*-THUMBNAIL.jpg`). Red, green and blue channels are extracted from EnMAP bands 43, 28 and 10 at wavelengths 634.919 nm, 550.525 nm and 463.584 nm, respectively.

### Quality Layers

The quality layers are stored in separate geotiff files (`*-QL_*.TIF`) with the quality information as listed below:

|        Quality Layer         |   0    |      1       |   2    |     3      |
| :--------------------------: | :----: | :----------: | :----: | :--------: |
|      `QL_PIXELMASK.TIF`      | Normal |  Defective   |        |            |
|   `QL_QUALITY_CIRRUS.TIF`    |  None  |     Thin     | Medium |   Thick    |
|   `QL_QUALITY_CLASSES.TIF`   |  None  |     Land     | Water  | Background |
|    `QL_QUALITY_CLOUD.TIF`    |  None  |    Cloud     |        |            |
| `QL_QUALITY_CLOUDSHADOW.TIF` |  None  | Cloud Shadow |        |            |
|    `QL_QUALITY_HAZE.TIF`     |  None  |     Haze     |        |            |
|    `QL_QUALITY_SNOW.TIF`     |  None  |     Snow     |        |            |
|        `QL_SWIR.TIF`         | Normal |  Defective   |        |            |
|        `QL_VNIR.TIF`         | Normal |  Defective   |        |            |

For the `QL_QUALITY_TESTFLAGS.TIF` quality layer see [EnMAP HSI Level 1 / Level 2 Product Specification Document](https://www.enmap.org/data/doc/EN-PCV-ICD-2009-2_HSI_Product_Specification_Level1_Level2.pdf).
