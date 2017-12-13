Marxan Connect
================

Marxan Connect (henceforth the "app") is a Graphical User Interface (GUI) to help conservationists include "connectivity" in their protected area network planning.

The term "connectivity" has a variety of definitions (i.e. larval connectivity, genetic connectivity, landscape connectivity, etc) and protected area networks can be optimized for various connectivity objectives. The app is intended to guide conservationists through the process of identifying important aspects of connectivity for their conservation scenarios as well as highlighting the necessary data.

The app also includes a fully functional Python module (in progress) that is operated via command line. The Python module, [`marxanconpy`](https://github.com/remi-daigle/MarxanConnect/blob/master/marxanconpy.py), can be used to reproduce an analysis using the project file generated by the GUI.

To use this software, please visit the [Tutorial](https://remi-daigle.github.io/MarxanConnect/tutorial) and the [Glossary](https://remi-daigle.github.io/MarxanConnect/glossary) (both in progress). Otherwise, if you would just like to get started, please install the app and proceed through all the tabs from left to right starting the "Spatial Input". After calculating the "Connectivity Metrics", you can choose to conduct a Marxan analysis in the app, export the connectivity metrics for use in a standalone custom Marxan analysis, or you can visualize the Connectivity Metrics using the "Plotting Options" tab

If you would like to report any bugs or request a missing feature, please post an issue on the GitHub repository or [email](mailto:remi.daigle@dal.ca?subject=Marxan%20with%20Connectivity%20bug%20or%20feature%20request) (although GitHub is preferred). Please provide as much information as possible, such as: detailed description, app version, operating system, even a link to your data if relevant (also, see [Contributing](https://remi-daigle.github.io/MarxanConnect/#contributing)).

Installing
==========

Windows Installer
-----------------

(**WARNING! Marxan Connect is in 'alpha' release and is not yet fully operational, download at your own risk**)

Please download the latest [MarxanConnect-vX-Y-Z-windows-setup.exe](https://github.com/remi-daigle/MarxanConnect/releases) installer file, run it, and follow the instructions. Alternatively (for advanced users only), follow the [Building from source](https://remi-daigle.github.io/MarxanConnect/#building-from-source) instructions to use the latest bleeding edge version of the app.

Windows Zipped Bundle
---------------------

If you cannot use the installer because you do not have administrative privileges, we've provided a zipped bundle of the app to allow users to bypass that problem. To use, download the latest [MarxanConnect.zip](https://github.com/remi-daigle/MarxanConnect/releases), unzip it to your preferred destination (e.g. `~/Desktop`), and double-click `MarxanConnectGUI.exe`. In this case you will have to generate any start menu shortcuts, or file associations (i.e. `.MarCon`) manually.

Building from source
====================

Building from source is only necessary if you plan to contribute to the project (see [Contributing](https://remi-daigle.github.io/MarxanConnect/#contributing) section below) or if you want to use the bleeding edge version of the app.

Building this repository has only been tested on Python 3.5.2 64-bit on a machine running Windows 10, your mileage may vary! (*Please note, I could not build the app using Anaconda*).

-   Download this repository
-   If necessary, edit the hard coded file paths in [setup.py](https://github.com/remi-daigle/MarxanConnect/blob/master/setup.py) and [WindowsSetupBuilder.iss](https://github.com/remi-daigle/MarxanConnect/blob/master/WindowsSetupBuilder.iss)
-   open a terminal or `cmd` window (or git bash) in the project directory and type:

<!-- -->

    make

Prerequisites (for building from source)
----------------------------------------

-   [Python 3.5.2 64-bit](https://www.python.org/downloads/release/python-352/)
-   [wxFormBuilder](https://github.com/wxFormBuilder/wxFormBuilder)
-   [Inno Setup](http://www.jrsoftware.org/isinfo.php)
-   [R](https://www.r-project.org/) and the [`rmarkdown`](http://rmarkdown.rstudio.com/) package

It also assumes you have all the pre-requisite python modules installed, i.e.:

    #!/bin/bash
    # for basic GUI
    pip install wxpython
    pip install matplotlib
    pip install matplotlib.basemap
    pip install geopandas
    pip install descartes
    pip install python-igraph
    pip install networkx

    # for compiling executable
    pip install cx_Freeze

Built With
==========

The `gui.py` file was built using the fantastic [wxFormBuilder](https://github.com/wxFormBuilder/wxFormBuilder).

The windows installer was built using [Inno Setup](http://www.jrsoftware.org/isinfo.php).

THe documentation and website was built with [R](https://www.r-project.org/) and the [`rmarkdown`](http://rmarkdown.rstudio.com/) package

Contributing
============

Please read [CONTRIBUTING.md](https://remi-daigle.github.io/MarxanConnect/CONTRIBUTING) for details on our code of conduct, and the process for submitting pull requests or issues to us.

Versioning
==========

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/remi-daigle/MarxanConnect/tags).

Authors
=======

-   **Remi Daigle** - *Initial work, development, maintenance* - [remi-daigle](https://github.com/remi-daigle)
-   **Anna Metaxas** - *Consultation*
-   **Arieanna Balbar** - *Consultation* - [abalbar](https://github.com/abalbar)
-   **Jennifer McGowan** - *Consultation*
-   **Eric Anton Treml** - *Consultation*
-   **Caitie Kuempel** - *Consultation* - [cdkuempel](https://github.com/cdkuempel)
-   **Hugh Possingham** - *Consultation*
-   **Jo Clarke** - *Consultation*
-   **Maria Beger** - *Consultation*

See also the list of [contributors](https://github.com/remi-daigle/MarxanConnect/contributors) who participated in this project.

License
=======

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/remi-daigle/MarxanConnect/blob/master/LICENSE) file for details

Acknowledgments
===============

-   Funding for the development of this software was provided Canadian Healthy Oceans Network [(CHONe)](https://chone2.ca/) a Natural Sciences and Engineering Research Council of Canada [(NSERC)](http://www.nserc-crsng.gc.ca/index_eng.asp) Strategic Network.
-   This project builds on the existing [Marxan](http://marxan.net/) (Ball et al. 2009) software and would not be possible without the hard work of Ian Ball, Hugh Possingham, and Matt Watts.

References
==========

Ball, I.R., H.P. Possingham, and M. Watts. 2009. Marxan and relatives: Software for spatial conservation prioritisation. Chapter 14: Pages 185-195 in Spatial conservation prioritisation: Quantitative methods and computational tools. Eds Moilanen, A., K.A. Wilson, and H.P. Possingham. Oxford University Press, Oxford, UK.
