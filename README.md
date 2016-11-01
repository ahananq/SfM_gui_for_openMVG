#About 
This is a GUI (general user interface) for the SfM (Structure from Motion) pipelines of [openMVG](http://imagine.enpc.fr/~moulonp/openMVG/) and [openMVS](https://github.com/cdcseacave/openMVS). Also supporting [CMVS/PMVS](https://github.com/pmoulon/CMVS-PMVS) 
It's aim is to make it simple to do a state-of-the-art Structure from Motion Reconstrcution from photographic scenes, especially anatomic structures with FOSS (free and open source software). It is aimed for users with no or very limited knowledge of SfM pipelines and the terminal.

# Install & Usage
The GUI is curently only aimed and tested for Ubuntu 15.10.

For Building from the terminal on Ubuntu please see the [Building Page](https://github.com/open-anatomy/SfM_gui_for_openMVG/blob/master/BUILD.md).

Once the project is built, just run "cd ~/openMVG_build/Linux-x86_64-RELEASE && ./openMVG_SfM_gui" from the terminal or add a launcher to this location.

# Credits / License
[openMVG](https://github.com/openMVG/openMVG) is developed by Pierre Moulon - see [Authors](https://github.com/openMVG/openMVG/blob/master/AUTHORS). 
[openMVS](https://github.com/cdcseacave/openMVS) is developed by cdcseacave.
[CMVS/PMVS](https://github.com/pmoulon/CMVS-PMVS) is developed by Pierre Moulon. 
[Point Cloud Library](https://github.com/PointCloudLibrary) is used for Previews.

As a fork of openMVG the [openMVG Licence](https://github.com/openMVG/openMVG/blob/master/license.openMVG) applies.

# Preview
![Screenshot](https://github.com/open-anatomy/SfM_gui_for_openMVG/raw/master/docs/screenshot.png)

# Intention
This program is part of the [Open Anatomy Project](https://github.com/open-anatomy) and aimed to provide an easy-to-use Interface for the Reconstruction of anatomic structures from image sets. It can access the main features from openMVG and openMVS for these purposes. It's original intention was to become a part of openMVG, and the openMVG parts of it may be used for a pull request in the future.

# Acknowledgements & contact for openMVG
----------------
Acknowledgements
----------------

openMVG authors would like to thanks libmv authors for providing an inspiring 
base to design openMVG. Authors also would like to thanks Mikros Image [1] 
and LIGM-Imagine laboratory [2] for support and authorization to make this
library an opensource project.

[1] [http://www.mikrosimage.eu/](http://www.mikrosimage.eu/)
[2] [http://imagine.enpc.fr/](http://imagine.enpc.fr/)

---------
Contact
---------

openmvg-team[AT]googlegroups.com


---------
Citations
---------

If you find the library or some part of it useful, then following
publications are relevant:

[3] Moulon Pierre, Monasse Pascal and Marlet Renaud. ACCV 2012.
[Adaptive Structure from Motion with a contrario model estimation.](http://hal.archives-ouvertes.fr/index.php?halsid=1n2qdqiv2a0l5eq7qpos9us752&view_this_doc=hal-00769266&version=1)

[4] Moulon Pierre and Monasse Pascal. CVMP 2012.
[Unordered feature tracking made fast and easy.](http://hal.archives-ouvertes.fr/index.php?halsid=ggdarhl8cv1j6ohq2073eok8q3&view_this_doc=hal-00769267&version=1)

[5] Moisan Lionel, Moulon Pierre and Monasse Pascal. IPOL 2012.
[Automatic Homographic Registration of a Pair of Images, with A Contrario Elimination of Outliers.](http://dx.doi.org/10.5201/ipol.2012.mmm-oh)

[6] Moulon Pierre, Monasse Pascal and Marlet Renaud. ICCV 2013.
[Global Fusion of Relative Motions for Robust, Accurate and Scalable Structure from Motion.](http://imagine.enpc.fr/~moulonp/publis/iccv2013/index.html)

or cite it as:

```
  @misc{openMVG,
    author = "Pierre Moulon and Pascal Monasse and Renaud Marlet and Others",
     title = "OpenMVG. An Open Multiple View Geometry library.",
    howpublished = "\url{https://github.com/openMVG/openMVG}",
  }
```
