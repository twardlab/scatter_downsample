# scatter_downsample

This repository uses scattering transforms to downsample microscopy images without losing information about texture.

The resulting images have a low resolution, but a large number of features at each pixel.

Here we show an example using Nissl images from the Allen Reference Atlas.

Downsampling an image using standard 2x2 averaging, leads to the following:

![figure](figures/section_000227_11648_average.jpg)


Applying a scattering transform gives a high dimensional signal, rather than a red-green-blue image.

The first PCA component can be used to reconstruct the above image almost exactly:

![figure](figures/section_000227_11648_pc_0.jpg)

The further components can be mapped to red green and blue to reveal more detail.
![figure](figures/section_000227_11648_pc_1_3.jpg)
