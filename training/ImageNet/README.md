# ImageNet Training Recipe

This folder contains an example implementation of an ImageNet training recipe.  Check out the help by running `julia train_imagenet.jl --help`.  In order to train a large-scale computer vision model, you will need an extensive dataset.  We suggest downloading the ImageNet 2012 large-scale visual recognition challenge dataset, currently [downloadable from Kaggle](https://www.kaggle.com/c/imagenet-object-localization-challenge/data).

Once you have downloaded and extracfted the dataset, the data we are most interested in is located in the `ILSVRC/Data/CLS-LOC` directory, where there exist files such as `train/n01484850/n01484850_18231.JPEG` and `val/ILSVRC2012_val_00000003.JPEG`.  These `train` and `val` folders are what should be passed to `train_imagenet.jl` via the `--train-dir` and `--val-dir` options.  The structure of the data is important, as the filenames contain information necessary to identify which class the datapoint comes from.