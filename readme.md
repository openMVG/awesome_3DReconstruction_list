
# Awesome 3D reconstruction list [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

> A curated list of papers & resources linked to 3D reconstruction from images.

**Note that:**
- **This list is not exhaustive,**
- **Tables use alphabetical order for fairness.**

> If you look to a more generic computer vision awesome list please check [this list](https://github.com/jbhuang0604/awesome-computer-vision)

## Contents

- [Tutorials](#tutorials)

- [Papers](#papers)
	- [SLAM](#papers-slam)
	- [SFM](#papers-sfm)

		- [Incremental SfM](#papers-sfm-incremental)
		- [Global SfM](#papers-sfm-global)
		- [Hierarchical SfM](#papers-sfm-hierarchical)
		- [Non Rigid SfM](#papers-non-rigid-sfm)
<br/><br/>
		- [Viewing graph optimization](#papers-sfm-graph)
		- [Unordered feature tracking](#papers-sfm-tracking)
		- [Large scale image matching for SfM](#papers-sfm-large-scale-matching)

	- [Localization](#papers-localization)
		- [Real time localization in SfM reconstructions](#papers-localization-in-sfm)

	- [MVS](#papers-mvs)
		- [Point cloud computation](#papers-mvs-point-cloud)
		- [Surface computation & refinements](#papers-mvs-surface)
		- [Multiple View Mesh Texturing](#papers-mvs-texturing)
		
	- [UAV Trajectory Optimization for model completeness](#papers-uav-acquisition)

- [OpenSource software resources](#opensource)
	- [SfM](#opensource-sfm)
	- [Multiple View Geometry Library Solvers](#opensource-solvers)
	- [MVS (Multiple View Stereovision)](#opensource-mvs)
	- [SLAM](#opensource-slam)
	- [Large Scale Image Retrieval](#opensource-cbir)
	- [Minimization](#opensource-minimization)
	- [Nearest Neighbor Search](#opensource-nn)
	- [Mesh storage processing](#opensource-mesh)

- [Feature detection description](#features)

- [Datasets with ground truth - Reproducible research](#dataset)

- [License](#license)

- [Contributing](#contributing)

<a name="tutorials"></a>
# Tutorials

## SLAM Tutorial & survey

[Micro Flying Robots: from Active Vision to Event-based Vision](https://www.youtube.com/watch?v=Sh0MXi8XTNI) D. Scaramuzza.

[ICRA 2016 Aerial Robotics - (Visual odometry)](http://mrsl.grasp.upenn.edu/loiannog/tutorial_ICRA2016/VO_Tutorial.pdf) D. Scaramuzza

[Simultaneous Localization And Mapping: Present, Future, and the Robust-Perception Age](http://arxiv.org/pdf/1606.05830.pdf). C. Cadena, L. Carlone, H. Carrillo, Y. Latif, D. Scaramuzza, J. Neira, I. D. Reid, J. J. Leonard.
  - "The paper summarizes the outcome of the workshop “The Problem of Mobile Sensors: Setting future goals and indicators of progress for SLAM” held during the Robotics: Science and System (RSS) conference (Rome, July 2015)."


[Visual Odometry: Part I - The First 30 Years and Fundamentals](http://rpg.ifi.uzh.ch/docs/VO_Part_I_Scaramuzza.pdf), D. Scaramuzza and F. Fraundorfer, IEEE Robotics and Automation Magazine, Volume 18, issue 4, 2011

[Visual Odometry: Part II - Matching, robustness, optimization, and applications](http://rpg.ifi.uzh.ch/docs/VO_Part_II_Scaramuzza.pdf), F. Fraundorfer and D. Scaramuzza, IEEE Robotics and Automation Magazine, Volume 19, issue 2, 2012

## SfM tutorial
[Open Source Structure-from-Motion](http://www.kitware.com/cvpr2015-tutorial.html). M. Leotta, S. Agarwal, F. Dellaert, P. Moulon, V. Rabaud. CVPR 2015 Tutorial.

## MVS tutorial

[Multi-View Stereo: A Tutorial](http://www.cse.wustl.edu/~furukawa/papers/fnt_mvs.pdf). Y. Furukawa, C. Hernández. Foundations and Trends® in Computer Graphics and Vision, 2015.

[State of the Art 3D Reconstruction Techniques](https://docs.google.com/file/d/0B851Hlh7xL0KNGx3X09VcEYzSjg/preview) N. Snavely, Y. Furukawa, CVPR 2014 tutorial slides. [Introduction](http://www.cse.wustl.edu/~furukawa/papers/cvpr2014_tutorial_intro.pdf) [MVS with priors](http://www.cse.wustl.edu/~furukawa/papers/cvpr2014_tutorial_mvs_prior.pdf) - [Large scale MVS](http://www.cse.wustl.edu/~furukawa/papers/cvpr2014_tutorial_large_scale_mvs.pdf)

## RGB-D mapping
[3D indoor scene modeling from RGB-D data: a survey](http://cg.cs.tsinghua.edu.cn/papers/CVMJ-2015-scene-moddeling.pdf) K. Chen, YK. Lai and SM. Hu. Computational Visual Media 2015.

## All in one tutorial

[Introduction of Visual SLAM, Structure from Motion and Multiple View Stereo](http://www.slideshare.net/yuhuang/visual-slam-structure-from-motion-multiple-view-stereo). Yu Huang 2014.

## Computer vision books

[Computer Vision: Algorithms and Applications](http://szeliski.org/Book/). R. Szeliski. 2010.



<a name="papers"></a>
# Papers

<a name="papers-slam"></a>
## SLAM/VO

### Visual odometry (image based only)

[Real-time simultaneous localisation and mapping with a single camera](https://www.doc.ic.ac.uk/~ajd/Publications/davison_iccv2003.pdf). A. J. Davison. ICCV 2003.

[Visual odometry](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.137.4025&rep=rep1&type=pdf). D. Nister, O. Naroditsky, and J. Bergen. CVPR 2004.

[Real time localization and 3d reconstruction](http://maxime.lhuillier.free.fr/pCvpr06.pdf). E. Mouragnon, M. Lhuillier, M. Dhome, F. Dekeyser, and P. Sayd. CVPR 2006.

[Parallel Tracking and Mapping for Small AR Workspaces](http://www.robots.ox.ac.uk/~gk/publications/KleinMurray2007ISMAR.pdf). G. Klein, D. Murray. ISMAR 2007.

[Real-Time 6-DOF Monocular Visual SLAM in a Large-scale Environments](http://cvlab.hanyang.ac.kr/~jwlim/files/icra2014vslam.pdf). H. Lim, J. Lim, H. Jin Kim. ICRA 2014.

[Direct Sparse Odometry](https://www.arxiv.org/abs/1607.02565), J. Engel, V. Koltun, D. Cremers, arXiv:1607.02565, 2016.

[Visual SLAM algorithms: a survey from 2010 to 2016](https://link.springer.com/article/10.1186/s41074-017-0027-2), T. Taketomi, H. Uchiyama, S. Ikeda, IPSJ T Comput Vis Appl (2017)

<a name="papers-sfm"></a>
## SfM papers

<a name="papers-sfm-incremental"></a>
### Incremental SfM
[Photo Tourism: Exploring Photo Collections in 3D](http://phototour.cs.washington.edu/Photo_Tourism.pdf). N. Snavely, S. M. Seitz, and R. Szeliski.  SIGGRAPH 2006.

[Towards linear-time incremental structure from motion](http://ccwu.me/vsfm/vsfm.pdf). C. Wu. 3DV 2013.

[Structure-from-Motion Revisited](http://people.inf.ethz.ch/jschoenb/papers/schoenberger2016sfm.pdf). Schöenberger, Frahm. CVPR 2016.

<a name="papers-sfm-global"></a>
### Global SfM
[Combining two-view constraints for motion estimation](http://www.umiacs.umd.edu/users/venu/cvpr01.pdf) V. M. Govindu. CVPR, 2001.

[Lie-algebraic averaging for globally consistent motion estimation](http://www.umiacs.umd.edu/users/venu/cvpr04final.pdf). V. M. Govindu.  CVPR, 2004.

[Robust rotation and translation estimation in multiview reconstruction](http://imagine.enpc.fr/~monasse/Stereo/Projects/MartinecPajdla07.pdf). D. Martinec and T. Pajdla. CVPR, 2007.

[Non-sequential structure from motion](http://www.maths.lth.se/vision/publdb/reports/pdf/enqvist-kahl-etal-wovcnnc-11.pdf). O. Enqvist, F. Kahl, and C. Olsson. ICCV OMNIVIS Workshops 2011.

[Global motion estimation from point matches](https://web.math.princeton.edu/~amits/publications/sfm_3dimpvt12.pdf). M. Arie-Nachimson, S. Z. Kovalsky, I. KemelmacherShlizerman, A. Singer, and R. Basri. 3DIMPVT 2012.

[Global Fusion of Relative Motions for Robust, Accurate and Scalable Structure from Motion](https://hal-enpc.archives-ouvertes.fr/hal-00873504). P. Moulon, P. Monasse and R. Marlet. ICCV 2013.

[A Global Linear Method for Camera Pose Registration](http://www.cs.sfu.ca/~pingtan/Papers/iccv13_sfm.pdf). N. Jiang, Z. Cui, P. Tan. ICCV 2013.

[Global Structure-from-Motion by Similarity Averaging](http://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Cui_Global_Structure-From-Motion_by_ICCV_2015_paper.pdf). Z. Cui, P. Tan. ICCV 2015.

[Linear Global Translation Estimation from Feature Tracks](http://arxiv.org/abs/1503.01832) Z. Cui, N. Jiang, C. Tang, P. Tan, BMVC 2015.

<a name="papers-sfm-hierarchical"></a>
### Hierarchical SfM
[Structure-and-Motion Pipeline on a Hierarchical Cluster Tree](http://www.diegm.uniud.it/fusiello/papers/3dim09.pdf).  A. M.Farenzena, A.Fusiello, R. Gherardi. Workshop on 3-D Digital Imaging and Modeling, 2009.

[Randomized Structure from Motion Based on Atomic 3D Models from Camera Triplets](https://www.researchgate.net/publication/224579249_Randomized_structure_from_motion_based_on_atomic_3D_models_from_camera_triplets). M. Havlena, A. Torii, J. Knopp, and T. Pajdla. CVPR 2009.

[Efficient Structure from Motion by Graph Optimization](https://dspace.cvut.cz/bitstream/handle/10467/62206/Havlena_stat.pdf?sequence=1&isAllowed=y). M. Havlena, A. Torii, and T. Pajdla. ECCV 2010.

[Hierarchical structure-and-motion recovery from uncalibrated images](http://www.diegm.uniud.it/fusiello/papers/cviu15.pdf). Toldo, R.; Gherardi, R., Farenzena, M. and Fusiello, A.. CVIU 2015.

<a name="papers-non-rigid-sfm"></a>
### Non Rigid SfM

[Robust Structure from Motion in the Presence of Outliers and Missing Data](http://arxiv.org/abs/1609.02638). G. Wang, J. S. Zelek, J. Wu, R. Bajcsy. 2016.

<a name="papers-sfm-graph"></a>
### Viewing graph optimization

[Skeletal graphs for efficient structure from motion](http://www.cs.cornell.edu/~snavely/projects/skeletalset/). N. Snavely, S. Seitz, R. Szeliski. CVPR 2008

[Optimizing the Viewing Graph for Structure-from-Motion](http://homes.cs.washington.edu/~csweeney/papers/optimizing_the_viewing_graph.pdf). C. Sweeney, T. Sattler, M. Turk, T. Hollerer, M. Pollefeys. ICCV 2015

[Graph-Based Consistent Matching for Strucutre-from-Motion](https://home.cse.ust.hk/~tshenaa/files/pub/eccv2016_graph_match.pdf). T. Shen, S. Zhu, T. Fang, R. Zhang, L. Quan. ECCV 2016.

<a name="papers-sfm-tracking"></a>
### Unordered feature tracking

[Unordered feature tracking made fast and easy](http://imagine.enpc.fr/~moulonp/publis/featureTracking_CVMP12.pdf).  P. Moulon and P. Monasse. CVMP 2012.

[Point Track Creation in Unordered Image Collections Using Gomory-Hu Trees](http://www.maths.lth.se/vision/publdb/reports/pdf/svarm-simayijang-etal-i2-12.pdf). Svärm, Simayijiang, Enqvist, Olsson. ICPR 2012.

[Fast connected components computation in large graphs by vertex pruning](). A. Lulli, E. Carlini, P. Dazzi, C. Lucchese, and L. Ricci. IEEE Transactions on Parallel and Distributed Systems 2016.


<a name="papers-sfm-large-scale-matching"></a>
### Large scale image matching for SfM

[Video Google: A Text Retrieval Approach to Object Matching in Video](http://www.robots.ox.ac.uk/~vgg/research/vgoogle/). J. Sivic, F. Schaffalitzky and A. Zisserman. ICCV 2003.

[Scalable Recognition with a Vocabulary Tree](http://www.vis.uky.edu/~stewe/publications/nister_stewenius_cvpr2006.pdf). Nister, Stewenius, CVPR 2006.

[Building Rome in a Day](https://grail.cs.washington.edu/rome/rome_paper.pdf). S. Agarwal, N. Snavely, I. Simon,  S. M. Seitz, R. Szeliski. ICCV 2009.

[Product quantization for nearest neighbor search](https://hal.inria.fr/file/index/docid/825085/filename/jegou_pq_postprint.pdf). H. Jégou, M. Douze and C. Schmid. IEEE Transactions on Pattern Analysis and Machine Intelligence, 2011.

[Fast and Accurate Image Matching with Cascade Hashing for 3D Reconstruction](http://www.nlpr.ia.ac.cn/jcheng/papers/CameraReady-CasHash.pdf). J. Cheng, C. Leng, J. Wu, H. Cui, H. Lu. CVPR 2014. 

[Recent developments in large-scale tie-point matching](https://www.infona.pl/resource/bwmeta1.element.elsevier-3a6310b2-2ad0-3bdd-839d-8daecaca680d/content/partDownload/8900b0c7-b69c-39dc-8cbd-94217452a25f). Hartmann, Havlena, Schindler. ISPRS 2016.


<a name="papers-localization"></a>
## Localization

<a name="papers-localization-in-sfm"></a>
### Real time localization in SfM reconstructions

[Real-time Image-based 6-DOF Localization in Large-Scale Environments](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/limcvpr12.pdf). Lim, Sinha, Cohen, Uyttendaele. CVPR 2012. 

[Get Out of My Lab: Large-scale, Real-Time Visual-Inertial Localization](http://www.roboticsproceedings.org/rss11/p37.pdf). Lynen, Sattler, Bosse, Hesch, Pollefeys, Siegwart. RSS 2015. 


<a name="papers-mvs"></a>
## Multiple View Stereovision

<a name="papers-mvs-point-cloud"></a>
### Point cloud computation

[Accurate, Dense, and Robust Multiview Stereopsis](http://www.cs.wustl.edu/~furukawa/papers/cvpr07a.pdf). Y. Furukawa, J. Ponce. CVPR 2007. [PAMI 2010](http://www.cs.wustl.edu/~furukawa/papers/pami08a.pdf)

[State of the art in high density image matching](https://www.researchgate.net/publication/263465866_State_of_the_art_in_high_density_image_matching﻿). F. Remondino, M.G. Spera, E. Nocerino, F. Menna, F. Nex . The Photogrammetric Record 29(146), 2014.

[Progressive prioritized multi-view stereo](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Locher_Progressive_Prioritized_Multi-View_CVPR_2016_paper.pdf). A. Locher, M. Perdoch and L. Van Gool. CVPR 2016. 

[Pixelwise View Selection for Unstructured Multi-View Stereo](http://people.inf.ethz.ch/jschoenb/papers/schoenberger2016mvs.pdf﻿). J. L. Schönberger, E. Zheng, M. Pollefeys, J.-M. Frahm. ECCV 2016.


<a name="papers-mvs-surface"></a>
### Surface computation & refinements

[Efficient Multi-View Reconstruction of Large-Scale Scenes using Interest Points, Delaunay Triangulation and Graph Cuts](http://www.di.ens.fr/sierra/pdfs/07iccv_a.pdf). P. Labatut, J-P. Pons, R. Keriven. ICCV 2007

[Multi-View Stereo via Graph Cuts on the Dual of an Adaptive Tetrahedral Mesh](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/SinhaICCV07.pdf). S. N. Sinha, P. Mordohai and M. Pollefeys. ICCV 2007.

[Towards high-resolution large-scale multi-view stereo](https://www.researchgate.net/publication/221364700_Towards_high-resolution_large-scale_multi-view_stereo).  H.-H. Vu, P. Labatut, J.-P. Pons, R. Keriven. CVPR 2009.

[Refinement of Surface Mesh for Accurate Multi-View Reconstruction](http://cmp.felk.cvut.cz/ftp/articles/tylecek/Tylecek-IJVR2010.pdf). R. Tylecek and R. Sara. IJVR 2010.

[High Accuracy and Visibility-Consistent Dense Multiview Stereo]().  H.-H. Vu, P. Labatut, J.-P. Pons, R. Keriven. Pami 2012.

[Exploiting Visibility Information in Surface Reconstruction to Preserve Weakly Supported Surfaces](https://www.researchgate.net/publication/275064596_Exploiting_Visibility_Information_in_Surface_Reconstruction_to_Preserve_Weakly_Supported_Surfaces) M. Jancosek et al. 2014.

[A New Variational Framework for Multiview Surface Reconstruction](http://urbanrobotics.net/pdf/A_New_Variational_Framework_for_Multiview_Surface_Reconstruction_86940719.pdf). B. Semerjian. ECCV 2014.

[Photometric Bundle Adjustment for Dense Multi-View 3D Modeling](https://www.inf.ethz.ch/personal/pomarc/pubs/DelaunoyCVPR14.pdf). A. Delaunoy, M. Pollefeys. CVPR2014.

[Global, Dense Multiscale Reconstruction for a Billion Points](https://lmb.informatik.uni-freiburg.de/people/ummenhof/multiscalefusion/). B. Ummenhofer, T. Brox. ICCV 2015.

[Efficient Multi-view Surface Refinement with Adaptive Resolution Control](http://home.cse.ust.hk/~slibc/pdf/arc.pdf). S. Li, S. Yu Siu, T. Fang, L. Quan. ECCV 2016.

[Multi-View Inverse Rendering under Arbitrary Illumination and Albedo](http://www.ok.ctrl.titech.ac.jp/~torii/project/mvir/), K. Kim, A. Torii, M. Okutomi, ECCV2016.

[Shading-aware Multi-view Stereo](http://www.gcc.tu-darmstadt.de/media/gcc/papers/Langguth-2016-SMV.pdf), F. Langguth and K. Sunkavalli and S. Hadap and M. Goesele, ECCV 2016.

[Scalable Surface Reconstruction from Point Clouds with Extreme Scale and Density Diversity](https://arxiv.org/abs/1705.00949), C. Mostegel, R. Prettenthaler, F. Fraundorfer and H. Bischof. CVPR 2017.

<a name="papers-mvs-texturing"></a>
### Multiple View Mesh Texturing

[Seamless image-based texture atlases using multi-band blending](http://imagine.enpc.fr/publications/papers/ICPR08a.pdf). C. Allène,  J-P. Pons and R. Keriven. ICPR 2008.

[Let There Be Color! - Large-Scale Texturing of 3D Reconstructions](http://www.gcc.tu-darmstadt.de/home/proj/texrecon/). M. Waechter, N. Moehrle, M. Goesele. ECCV 2014.

<a name="papers-uav-acquisition"></a>
### UAV Trajectory Optimization for model completeness

[Submodular Trajectory Optimization for Aerial 3D Scanning](http://graphics.stanford.edu/papers/aerial_scanning/). M. Roberts, A. Truong, D. Dey, S. Sinha, A. Kapoor, N. Joshi, P. Hanrahan. 2017.

<a name="opensource"></a>
# OpenSource resources


<a name="opensource-sfm"></a>
## OpenSource SfM (Structure from Motion)

| Project |  Language | License |
| ---  | --- | --- |
|[Bundler](https://github.com/snavely/bundler_sfm) | C++ | GNU General Public License - contamination|
|[Colmap](https://github.com/colmap/colmap) | C++ | GNU General Public License - contamination|
|[MAP-Tk](https://github.com/Kitware/maptk) | C++ | BSD 3-Clause license - Permissive |
|[MicMac](https://github.com/micmacIGN) | C++ | CeCILL-B |
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
|[MICMAC](http://logiciels.ign.fr/?Micmac) | C++ | CeCILL-B |
[MVE](https://github.com/simonfuhrmann/mve) | C++ | BSD 3-Clause license + parts under the GPL 3 license|
[OpenMVS](https://github.com/cdcseacave/openMVS/) | C++  (CUDA optional) | AGPL3|
[PMVS](https://github.com/pmoulon/CMVS-PMVS) | C++ CUDA | GNU General Public License - contamination|
[SMVS Shading-aware Multi-view Stereo](https://github.com/flanggut/smvs) | C++ | BSD-3-Clquse license |


<a name="opensource-slam"></a>
## OpenSource SLAM (Simultaneous Localization And Mapping)

| Project |  Language | License |
| ---  | --- | --- |
|[COSLAM](http://drone.sjtu.edu.cn/dpzou/project/coslam.php) | C++ |  GNU General Public License|
|[DSO-Direct Sparse Odometry](https://github.com/JakobEngel/dso) | C++ |  GPLv3|
|[DTSLAM-Deferred Triangulation SLAM](https://github.com/plumonito/dtslam) | C++ |  modified BSD|
|[LSD-SLAM](https://github.com/tum-vision/lsd_slam/) | C++/ROS |  GNU General Public License|
|[OKVIS: Open Keyframe-based Visual-Inertial SLAM](https://github.com/ethz-asl/okvis) | C++ | BSD|
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
## OpenSource minimization

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
|[Libnabo](https://github.com/ethz-asl/libnabo) | C++ | BSD License|
|[Nanoflann](https://github.com/jlblancoc/nanoflann) | C++ |  BSD License|

<a name="opensource-mesh"></a>
## Mesh storage processing

| Project |  Language | License|
| ---  | --- | --- |
[3DTK](http://slam6d.sourceforge.net/) | C++ | GPLv3|
|[CGAL](http://www.cgal.org/) | C++ |  Module dependent GPL/LGPL |
|[InstantMesh](https://github.com/wjakob/instant-meshes) Mesh Simplification| C++ | BSD License |
|[GEOGRAM](http://alice.loria.fr/software/geogram/doc/html/index.html/) | C++ | Revised BSD License |
|[libigl](http://libigl.github.io/libigl/tutorial/tutorial.html)| C++ | MPL2 |
|[Mesh-processing-library](https://github.com/Microsoft/Mesh-processing-library)| C++ | MIT License |
|[OpenMesh](http://www.openmesh.org/) | C++ | BSD 3 clause license|
|[PCL](http://www.pointclouds.org/)|C++|3-clause BSD license |
|[VCG](http://vcg.isti.cnr.it/~cignoni/newvcglib/html/)|C++|GPL |


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
|[LATCH](http://arxiv.org/pdf/1501.03719.pdf)| |x|
|MOPS | | x|
|[PhonySift](http://www.icg.tugraz.at/Members/gerhard/mvc/MVC_08_Tracking.pdf) | Multi-scale Fast | Reduced Sift grid|
|ORB|Multiscale Fast|Oriented BRIEF|

<a name="dataset"></a>
# Datasets with ground truth - Reproducible research

## Feature detection/description repeatability

[VGG Oxford](http://www.robots.ox.ac.uk/~vgg/research/affine/) 8 dataset with GT homographies + matlab code.

[Hannover - Region Detector Evaluation Data Set](http://www.tnt.uni-hannover.de/project/feature_evaluation/) Similar to the previous (5 dataset). Datasets have multiple image resolution & an increased GT homographies precision.

[DTU - Robot Image Data Sets - Point Feature Data Set](http://roboimagedata.compute.dtu.dk/?page_id=24) 60 scenes with know calibration & different illuminations.

## Corresponding interest point patches for descriptor learning
Corresponding patches, saved with a canonical scale and orientation.

[Multi-view Stereo Correspondence Dataset](http://www.cs.ubc.ca/~mbrown/patchdata/patchdata.html)

[HPatches](https://github.com/featw/hpatches) Dataset linked to the ECCV16 workshop "Local Features: State of the art, open problems and performance evaluation"

## Monocular odometry dataset

[Mono dataset](http://vision.in.tum.de/data/datasets/mono-dataset) 50 real-world sequences. Dataset linked to the DSO Visual Odometry paper.

## MVS - Point Cloud - Surface accuracy

[Middlebury Multi-view Stereo](http://vision.middlebury.edu/mview/) See "A Comparison and Evaluation of Multi-View Stereo Reconstruction Algorithms". CVPR 2006.

[Dense MVS](http://cvlabwww.epfl.ch/data/multiview/) See "On Benchmarking Camera Calibration and Multi-View Stereo for High Resolution Imagery". CVPR 2008.

[DTU - Robot Image Data Sets -MVS Data Set](http://roboimagedata.compute.dtu.dk/?page_id=36) See “Large Scale Multi-view Stereopsis Evaluation“. CVPR 2014.

 [A Multi-View Stereo Benchmark with High-Resolution Images and Multi-Camera Videos in Unstructured Scenes](http://people.inf.ethz.ch/sattlert/publications/Schoeps2017CVPR.pdf), T. Schöps, J. L. Schönberger, S. Galiani, T. Sattler, K. Schindler, M. Pollefeys, A. Geiger,. CVPR 2017.

[Tanks and Temples: Benchmarking Large-Scale Scene Reconstruction](http://vladlen.info/publications/tanks-temples-benchmarking-large-scale-scene-reconstruction/), A. Knapitsch, J. Park, Q.Y. Zhou and V. Koltun. SIGGRAPH 2017.


# License

License [![CCBY-SA](https://i.creativecommons.org/l/by-sa/4.0/80x15.png)]()

To the extent possible under law, [Pierre Moulon](https://github.com/pmoulon) has waived all copyright and related or neighboring rights to this work.

# Contributing
Please see [CONTRIBUTING](https://github.com/openMVG/awesome_3DReconstruction_list/blob/master/contributing.md) for details.




