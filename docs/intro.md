# AMHCT Bio-Image Analysis

This page contains the resources for the lecture "Navigating the Reproducibility Storm with Bio-Image Analysis" in the Advanced Methods & Human Cell Technologies (AMHCT) as part of the [Regenerative Biology and Medicine Master's Program](https://tu-dresden.de/cmcb/bildung-und-karriere/masters-courses/regenerative-biology-and-medicine).

## Lecture Content

This course will introduce the participants to the basics of bio-image analysis and processing in microscopy using open-source software. The course will cover the following topics:

- Installation and introduction to [napari](https://napari.org/stable/)
- Loading images from OMERO with [napari-omero](https://github.com/tlambert03/napari-omero)
- Segmentation with Machine Learning using [napari-apoc](https://github.com/haesleinhuepf/napari-accelerated-pixel-and-object-classification)
- Quick view into [micro-sam](https://github.com/computational-cell-analytics/micro-sam)
- Feature Extraction with [napari-skimage-regionprops](https://github.com/haesleinhuepf/napari-skimage-regionprops)
- Object Classification with Machine Learning using [napari-apoc](https://github.com/haesleinhuepf/napari-accelerated-pixel-and-object-classification) and [napari-clusters-plotter](https://github.com/BiAPoL/napari-clusters-plotter)
- Reproducible image analysis with [napari](https://napari.org/stable/) and [omero](https://omero.org/) using [napari-apoc](https://github.com/haesleinhuepf/napari-accelerated-pixel-and-object-classification) and [napari-omero](https://github.com/tlambert03/napari-omero)

## Logging in to OMERO

1. Download the [OMERO Insight application](https://www.openmicroscopy.org/omero/downloads/) and install it on your computer. This application allows you to connect to the OMERO server and upload images (the web interface cannot be used to upload images).

2. Connect to the CMCB VPN if you are not already connected. You can find the instructions for this [here](https://intranet.crt-dresden.de/grav/it_department/faq_howto/remote-connectivity-vpn-sftp-ssh) (internal link, needs ZIH login to be accessed).

3. Open the OMERO Insight application, click on the wrench icon and add the following server address `omero-int.biotec.tu-dresden.de`. This is the address of the OMERO server you will be using during the course.

```{image} ./napari_apoc_omero_workflow/apoc_omero_1.png
:alt: OMERO Insight
:width: 300px
:align: center
```

Use your ZIH credentials to log in.

## Setting up the environment

To follow the course, you will need to have Python installed in your computer. 

1. Install [Miniforge](https://conda-forge.org/download/)
   - Download the installer for your operating system (Windows, macOS, or Linux).
   - Follow the installation instructions for your operating system.

2. Open a terminal (preferably Miniforge Prompt, but not necessarily) and run the following command to clone/download the course repository to your computer:

```bash
git clone https://github.com/BiAPoL/AMHCT_Bio_Image_Analysis_2025.git
```

Alternatively, you can download the repository as a `.zip` file by clicking on the green "Code" button on the top right of the repository page and selecting "Download ZIP". Remember the place where you decompress the file for the next steps.

3. Navigate to the course repository:

```bash
cd AMHCT_Bio_Image_Analysis_2025
```

If you chose to download the `.zip` file in the previous step, you will need to navigate to the folder where you decompressed the file.

4. Install the required Python packages with:

```bash
mamba env create -f environment.yml
```

This creates a new environment called `amhct` and installs all the required packages.

5. Activate the environment:

```bash
mamba activate amhct
```

This will activate the environment, which means giving access to the path where the installed packages are.

You should see the name `(amhct)` now in front of the active typing line.

## Starting napari

You can now start napari by typing:

```bash
napari
```

in the terminal. The first time you start napari may take longer than usual.

If you have issues with pyclesperanto, check out this [troubleshooting section](https://github.com/clEsperanto/pyclesperanto_prototype?tab=readme-ov-file#troubleshooting-graphics-cards-drivers).