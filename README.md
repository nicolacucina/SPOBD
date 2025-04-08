This Repository contains code that implements the compressive sampling problem applied to the analysis of 2D images.
Each notebook approches the problem differently:
- `1D_DCT.ipynb`: In this notebook the image is processed scanning each row or column individually. This leads to a decoupling of the problems, which can be solved independently. The DCT is used to compress the image, and the results are compared with the original image.
- `2D_DCT.ipynb`: In this notebook the image is processed using patches. The DCT is used to compress the image, and the results are compared with the original image.
- `2D_DCT_overlap.ipynb`: In this notebook the image is processed using patches with overlap. The DCT is used to compress the image, and the results are compared with the original image.

A summary of the results obtained in each notebook is presented below:

Errors(average):
| $\downarrow$ **Notebook** / **Compression Ratio** $\rightarrow$ | **10%** | **20%**  | **30%**       | **40%**       | **50%**       |
|-----------------------------------------|-----------|-----------|-----------|-----------|-----------|
| 1D-DCT using Rows  | 1497.778       | 685.113         | 374.315 | 234.151         | 147.047 |
| 1D-DCT using Columns| 941.587     | 441.259       | 258.845   | 164.318      | 103.483 |
| 2D-DCT without overlap  | 369.307       | 173.616       | 106.294     | 71.500         | 47.005 |
| 2D-DCT with overlap and padding| 396.037      | 190.650            | 116.173   |  77.186     | 56.381|

Sparsities(average):
| $\downarrow$ **Notebook** / **Compression Ratio** $\rightarrow$ | **10%** | **20%**  | **30%**       | **40%**       | **50%**       |
|-----------------------------------------|-----------|-----------|-----------|-----------|-----------|
| 1D-DCT using Rows  | 26.697 |  52.285 |  77.492 |  102.568 | 128.52539062 |
| 1D-DCT using Columns| 26.172 |    51.939 |  77.791 | 102.783 | 128.890 | 
| 2D-DCT without overlap  | 13.579 | 25.941 | 38.998 | 51.806 | 64.783 |
| 2D-DCT with overlap and padding| 14.979 | 29.465 | 44.328 | 59.024 | 72.598