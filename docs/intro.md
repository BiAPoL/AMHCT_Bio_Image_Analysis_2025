# AMHCT Bio-Image Analysis

This page contains the resources for the lecture "Navigating the Reproducibility Storm with Bio-Image Analysis" in the Advanced Methods & Human Cell Technologies (AMHCT) as part of the [Regenerative Biology and Medicine Master's Program](https://tu-dresden.de/cmcb/bildung-und-karriere/masters-courses/regenerative-biology-and-medicine).

## Course Description

This course will introduce the participants to the basics of bio-image analysis and processing in microscopy using open-source software. The course will cover the following topics:

- Installation and introduction to [napari](https://napari.org/stable/)
- Loading images from OMERO with [napari-omero](https://github.com/tlambert03/napari-omero)
- Segmentation with Machine Learning using [napari-apoc](https://github.com/haesleinhuepf/napari-accelerated-pixel-and-object-classification), [micro-sam](https://github.com/computational-cell-analytics/micro-sam) and [napari-nninteractive](https://github.com/MIC-DKFZ/napari-nninteractive)
- Feature Extraction with [napari-skimage-regionprops](https://github.com/haesleinhuepf/napari-skimage-regionprops)
- Object Classification with Machine Learning using [napari-apoc](https://github.com/haesleinhuepf/napari-accelerated-pixel-and-object-classification) and [napari-clusters-plotter](https://github.com/BiAPoL/napari-clusters-plotter)
- Reproducible image analysis with [napari](https://napari.org/stable/) and [omero](https://omero.org/) using [napari-apoc](https://github.com/haesleinhuepf/napari-accelerated-pixel-and-object-classification) and [napari-omero](https://github.com/tlambert03/napari-omero)

## Setting up the environment

To follow the course, you will need to have Python installed in your computer. 

1. Follow the instruction in [this blog post](https://biapol.github.io/blog/mara_lampert/getting_started_with_miniforge_and_python/readme.html) and stop before the "Creating a virtual environment" section.

2. Open a terminal (preferably Miniforge Prompt, but not necessarily) and run the following command to clone/download the course repository to your computer:

```bash
git clone https://github.com/BiAPoL/TrendsInMicroscopy_2025.git
```

Alternatively, you can download the repository as a `.zip` file by clicking on the green "Code" button on the top right of the repository page and selecting "Download ZIP". Remember the place where you decompress the file for the next steps.

3. Navigate to the course repository:

```bash
cd TrendsInMicroscopy_2025
```

If you chose to download the `.zip` file in the previous step, you will need to navigate to the folder where you decompressed the file.

4. Install the required Python packages with:

```bash
mamba env create -f environment.yml
```

This creates a new environment called `tim25` and installs all the required packages.

5. Activate the environment:

```bash
mamba activate tim25
```

This will activate the environment, which means giving access to the path where the installed packages are.

You should see the name `(tim25)` now in front of the active typing line.

## Starting napari

You can now start napari by typing:

```bash
napari
```

in the terminal. The first time you start napari may take longer than usual.

## Starting Jupyter Lab

If you want to program jupyter notebooks, you can use [Jupyter Lab](https://jupyter.org/) as your platform to do so. We will use this in the last part of this course for scientific plotting. To start it, type:

```bash
jupyter lab
```

This should open a new tab in your default browser with the Jupyter Lab interface.