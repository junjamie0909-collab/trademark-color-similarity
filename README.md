# Measuring trademark color similarity

How typical are a drawing’s colors among the designs filed in the same year? This short Python notebook illustrates the color measure used in a study of U.S. trademark filings. It runs offline with six synthetic drawings. The example scores come entirely from those drawings.

[Open the notebook](Trademark_Color_Similarity_Demo.ipynb)

## How it works

1. Create two sets of drawings with the same red and blue pigments but different color frequencies.
2. Convert sRGB pixels to CIELAB, remove the light neutral background, and summarize the foreground in a normalized 144-bin color histogram.
3. Average the histograms within each year and calculate each drawing’s cosine similarity to its own year’s average, including the drawing itself.

The same red circle scores 0.894 when red is common and 0.447 when it is rare. Changing the comparison year changes what counts as typical. A red circle and a red square can have the same color score because this measure records color frequencies.

## Running the example

Open the notebook in Jupyter and run the cells from top to bottom with Python 3, NumPy, and Pillow. No account, data download, or API key is needed.
