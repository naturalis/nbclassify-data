Supplementary data
------------------

[![DOI](https://zenodo.org/badge/doi/10.5281/zenodo.31904.svg)](http://dx.doi.org/10.5281/zenodo.31904)

This repository contains supplementary data for the manuscript "OrchID: a
Generalized Framework for Taxonomic Classification of Images Using Evolved
Artificial Neural Networks".

In this repository you will find the following data:

* cache/
    Cached phenotypes for the configurations from config.yml.

* images/
    Would normally contain the image collection (not included here, but can
    upon request be download from our private Flickr account). The
    ``nbc-trainer`` script is used to create a meta-data file for the image
    collection. This meta-data file is included (``.meta.db``, sqlite3
    database), and can (along with the phenotype cache) be used to run
    ``nbc-trainer validate`` to perform the cross-validation analyses.

* orchid.ann/
    Directory containing a hierarchy of artificial neural networks trained on
    the collection of slipper orchid images from our Flickr account.

* output/
    Contains the cross-validation results. There are two subdirectories: ``k4*``
    and ``k10*`` contain the results for 4-fold and 10-fold cross-validation,
    respectively. Each of these folders contain the following subdirectories:

    `ann`
        Trained neural networks for each fold.

    `results`
        The classification results for each fold.

    `test`
        Test data used for each fold.

    `train`
        Training data used for each fold.

    These directories were automatically created with ``nbc-trainer validate``
    (see the nbclassify documentation for details), for example::

        nbc-trainer config.yml validate -c cache/ -k4 --autoskip images/

    Because the classification results in the "results" subdirectory are
    difficult to interpret, we used several scripts (``nbc-scores`` and
    ``nbc-scores-r`` from the nbclassify repository) to summarize these
    results. The files ``summary-k4.txt`` and ``summary-k10.txt`` contain the
    summarized results for 4-fold and 10-fold cross-validation, respectively.

* config.yml
    The configurations file used to generate the aforementioned data. If you
    run ``nbc-trainer`` with this configurations file (unmodified), it can use
    the cache from the "cache" directory to generate training data (without
    needing to download the complete image collection). If you change the
    configurations in this file (especially the configurations for
    ``features``), then ``nbc-trainer`` will create a new cache and extract the
    features from the images (so the images must be present in the "images"
    directory in that case).

