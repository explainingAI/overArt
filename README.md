# OverArt dataset

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.14524249.svg)](https://doi.org/10.5281/zenodo.14524249)


<div align="center">
  <img src="https://raw.githubusercontent.com/explainingAI/overArt/master/docs/overart.png">
</div>

## Algorithm

We generate the OverArt dataset in order to obtain a ground truth of the concave points of 
overlapped objects. Each image of the dataset contains a cluster with three overlapped ellipses. 
The use of three ellipses is a good trade-off between complexity and reality. The proposed method to
detect concave points is only necessary when there are at least two overlapped objects, combination 
that is the most commonly found in the different clusters.

The ellipses of each image are defined by three parameters: the rotation, the feret diameter size 
and its center. The values of this parameters are generated randomly by the set of constraints 
described in Table I. This constrains are completed with the next restriction: none of the three 
cells must be outside the cluster. The first ellipse is located in the center of the image. The
positions of the other two ellipses are related to the first one. The location of the second ellipse 
is randomly selected inside the area defined by the minimum and maximum distance to the center of 
the first ellipse. Finally, the third one is randomly placed inside the area defined by the minimum 
and maximum distance to the center of the first and second ellipses.

## Reference

### Article
```
@article{miro2020segmenting,
  title={Segmenting overlapped cell clusters in biomedical images by concave point detection},
  author={Mir{\'o}-Nicolau, Miquel and Moy{\`a}-Alcover, Biel and Gonz{\'a}lez-Hidalgo, Manuel and Jaume-i-Cap{\'o}, Antoni},
  journal={arXiv preprint arXiv:2008.00997},
  year={2020}
}

```

### Database

```
@dataset{miro_nicolau_2024_14524249,
  author       = {Miró Nicolau, Miquel and
                  Moya-Alcover, Gabriel and
                  González-Hidalgo, Manuel and
                  Jaume-i-Capó, Antoni},
  title        = {OverArt dataset},
  month        = dec,
  year         = 2024,
  publisher    = {Zenodo},
  version      = {1.0},
  doi          = {10.5281/zenodo.14524249},
  url          = {https://doi.org/10.5281/zenodo.14524249},
}
```