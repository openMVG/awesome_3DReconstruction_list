
# Awesome 3D reconstruction list [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

> A curated list of papers & ressources linked to 3D reconstruction from images. awesome collection of papers & ressources linked to 3D reconstruction from images

**Note that:**
- **This list is not exhaustive,**
- **Tables use alphabetical order for fairness.**

> If you look to a more generic computer vision awesome list please check [this list](https://github.com/jbhuang0604/awesome-computer-vision)

##Table of Contents
- [Papers & tutorials](#papers)
	- [slam](#papers-slam)
- [OpenSource software ressources](#opensource)
	- [SfM](#opensource-sfm)
	- [Multiple View Geometry Library Solvers](#opensource-solvers)
	- [MVS (Multiple View Stereovision)](#opensource-mvs)
	- [SLAM](#opensource-slam)
	- [Large Scale Image Retrieval](#opensource-cbir)
	- [Minimization](#opensource-minimization)
	- [Nearest Neighbor Search](#opensource-nn)

- [Feature detection description](#features)

- [License](#licence)

- [Contributing](#contributing)

<a name="papers"></a>
# Papers & tutorials

<a name="papers-slam"></a>
## SLAM/VO

### SLAM Tutorial & survey

[ICRA 2016 Aerial Robotics - (Visual odometry)](http://mrsl.grasp.upenn.edu/loiannog/tutorial_ICRA2016/VO_Tutorial.pdf) Davide Scaramuzza

[Simultaneous Localization And Mapping: Present, Future, and the Robust-Perception Age](http://arxiv.org/pdf/1606.05830.pdf). Cesar Cadena, Luca Carlone, Henry Carrillo, Yasir Latif, Davide Scaramuzza, José Neira, Ian D. Reid, John J. Leonard. "The paper summarizes the outcome of the workshop “The Problem of Mobile Sensors: Setting future goals and indicators of progress for SLAM” held during the Robotics: Science and System (RSS) conference (Rome, July 2015)."


[Visual Odometry [Tutorial]: Part I - The First 30 Years and Fundamentals](http://rpg.ifi.uzh.ch/docs/VO_Part_I_Scaramuzza.pdf), D. Scaramuzza and F. Fraundorfer, IEEE Robotics and Automation Magazine, Volume 18, issue 4, 2011
[Visual odometry: Part II - Matching, robustness, optimization, and applications](http://rpg.ifi.uzh.ch/docs/VO_Part_II_Scaramuzza.pdf), F. Fraundorfer and D. Scaramuzza,,  IEEE Robotics and Automation Magazine, Volume 19, issue 2, 2012


<a name="opensource"></a>
# OpenSource ressources


<a name="opensource-sfm"></a>
## OpenSource SfM (Structure from Motion)

| Project |  Language | License |
| ---  | --- | --- |
|[Bundler](https://github.com/snavely/bundler_sfm) | C++ | GNU General Public License - contamination|
|[Colmap](https://github.com/colmap/colmap) | C++ | GNU General Public License - contamination|
|[MVE](https://github.com/simonfuhrmann/mve) | C++ | BSD 3-Clause license + parts under the GPL 3 license|
|[OpenMVG](https://github.com/openMVG/openMVG) | C++ |  MPL2 - Permissive|
|[OpenSfM](https://github.com/mapillary/OpenSfM/) |  Python | Simplified BSD license - Permissive|
|[TheiaSfM](https://github.com/sweeneychris/TheiaSfM) | C++ |   New BSD license - Permissive|


<a name="opensource-solvers"></a>
## OpenSource Multiple View Geometry Library Solvers

| Project |  Language | License |
| ---  | --- | --- |
|[OpenGV](https://github.com/laurentkneip/opengv) | C++ | BSD - permissive |

<a name="opensource-mvs"></a>
## OpenSource MVS (Multiple View Stereovision)

| Project |  Language | License |
| ---  | --- | --- |
|[Colmap](https://github.com/colmap/colmap) | C++ CUDA |GNU General Public License - contamination|
[GPUIma + fusibile](https://github.com/kysucix) | C++ CUDA | GNU General Public License - contamination|
[HPMVS](https://github.com/alexlocher/hpmvs) | C++ | GNU General Public License - contamination|
[MVE](https://github.com/simonfuhrmann/mve) | C++ | BSD 3-Clause license + parts under the GPL 3 license|
[OpenMVS](https://github.com/cdcseacave/openMVS/) | C++  (CUDA optional) | AGPL3|
[PMVS](https://github.com/pmoulon/CMVS-PMVS) | C++ CUDA | GNU General Public License - contamination|

<a name="opensource-slam"></a>
## OpenSource SLAM (Simultaneous Localization And Mapping)

| Project |  Language | License |
| ---  | --- | --- |
|[COSLAM](http://drone.sjtu.edu.cn/dpzou/project/coslam.php) | C++ |  GNU General Public License|
|[DTSLAM-Deferred Triangulation SLAM](https://github.com/plumonito/dtslam) | C++ |  modified BSD|
|[LSD-SLAM](https://github.com/tum-vision/lsd_slam/) | C++/ROS |  GNU General Public License|
|[ORB-SLAM](https://github.com/raulmur/ORB_SLAM2) | C++ | GPLv3|
|[REBVO - Realtime Edge Based Visual Odometry for a Monocular Camera](https://github.com/JuanTarrio/rebvo) | C++ |  GNU General Public License | 
|[SVO semi-direct Visual Odometry](https://github.com/uzh-rpg/rpg_svo) | C++/ROS | GNU General Public License|

<a name="opensource-cbir"></a>
## Large scale image retrieval / CBIR (Content Based Image Retrieval)

| Project |  Language | License |
| ---  | --- | --- |
|[DBoW2](https://github.com/dorian3d/DBoW2) | C++ | modified BSD License|
|[libvot](https://github.com/hlzz/libvot) | C++ | BSD 3-Clause License|
|[VocabTree2](https://github.com/snavely/VocabTree2) | C++ | BSD License|

<a name="opensource-minimization"></a>
## OpenSource mimization

| Project |  Language | License |
| ---  | --- | --- |
|[CERES SOLVER](https://github.com/ceres-solver/ceres-solver) | C++ | BSD License|
|[GTSAM](https://collab.cc.gatech.edu/borg/gtsam) | C++ | BSD License|
|[G2O](https://github.com/RainerKuemmerle/g2o) | C++ |  BSD License + L/GPL3 restriction|
|[NLOPT](http://ab-initio.mit.edu/wiki/index.php/NLopt) | C++ | LGPL|

<a name="opensource-nn"></a>
## Nearest Neighbor Search

| Project |  Language | License|
| ---  | --- | --- |
|[ANN](http://www.cs.umd.edu/~mount/ANN/) | C++ | GNU General Public License|
|[Annoy](https://github.com/spotify/annoy) | C++ |  Apache License|
|[FLANN](http://www.cs.ubc.ca/research/flann/) | C++ | BSD License|
|[Nanoflann](https://github.com/jlblancoc/nanoflann) | C++ |  BSD License|


<a name="features"></a>
# Features

## Features detection/Description

| Project | Detection | Description |
| ---  | --- | --- |
|[AKAZE](https://github.com/pablofdezalc/akaze) |x|MSURF/MLDB|
|[DART](http://www.vision.cs.chubu.ac.jp/CV-R/pdf/MarimonCVPR2010.pdf) | x | x|
|[KAZE](https://github.com/pablofdezalc/kaze) |x|MSURF/MLDB|
|[LIOP/MIOP](https://github.com/foelin/IntensityOrderFeature) | |x|
|[LIFT (machine learning)](https://github.com/cvlab-epfl/LIFT) | x|x|
|MROGH | |x|
|SIFT |x|x|
|SURF |x|x|
|[SFOP](http://www.ipb.uni-bonn.de/data-software/sfop-keypoint-detector/) |x | |
|...  | | |

### "Real time" oriented methods

| Project | Detection | Description |
| ---  | --- | --- |
|BRIEF| |x|
|BRISK|x|x|
|FAST|x||
|FREAK| |x|
|FRIF|x|x|
|[HIPS](http://twd20g.blogspot.fr/2011/12/high-speed-feature-matching-with-simon.html) | | x|
|MOPS | | x|
|[PhonySift](http://www.icg.tugraz.at/Members/gerhard/mvc/MVC_08_Tracking.pdf) | Multiscale Fast | Reduced Sift grid|
|ORB|Multiscale Fast|Oriented BRIEF|

# License

License [![CCBY-SA](https://i.creativecommons.org/l/by-sa/4.0/80x15.png)]()

To the extent possible under law, [Pierre Moulon](https://github.com/pmoulon) has waived all copyright and related or neighboring rights to this work.

# Contributing
Please see [CONTRIBUTING](https://github.com/openMVG/awesome_3DReconstruction_list/blob/master/contributing.md) for details.





