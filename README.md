# Handwritten Text Recognition

A student computer vision project that converts scanned handwritten pages into text. It cleans page images with OpenCV, groups connected components into lines and symbols, and classifies the symbols with a PyTorch CNN trained on EMNIST Letters.

The original coursework run reported **90.86% letter classification accuracy** on a 5,000-image EMNIST test subset and a **15.86% character error rate** on the course pages. Connected letters were the main segmentation challenge. The page-level result depends on the input scans.

## Run the notebook

1. Install the requirements with `python -m pip install -r requirements.txt`.
2. Add your own light-on-dark handwritten PNG page images to `einstein_files/`. For a character error rate, add a matching `reference.txt` in page order.
3. Open `project.ipynb` in Jupyter and run the cells in order. The training cell downloads EMNIST and saves the trained classifier locally. The OCR cell writes the result to `pred_text.txt`.

The coursework scans, reference transcript, and model checkpoint are excluded from this repository.
