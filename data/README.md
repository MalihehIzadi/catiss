# Datasets

The original datasets can be obtained through:

```
curl "https://tickettagger.blob.core.windows.net/datasets/github-labels-top3-803k-train.tar.gz" | tar -xz
curl "https://tickettagger.blob.core.windows.net/datasets/github-labels-top3-803k-test.tar.gz" | tar -xz
```

To obtain the preprocessed datasets I used for training CatIss, 
run the `../notebooks/data_preprocess.ipynb` script on the original datasets.
I have also provided the cleaned test dataset here as `test_clean_concat_200.csv`.
The cleaned training set (which is much larger) is shared publicly on Google Drive:

```
https://drive.google.com/drive/folders/1jgV4U41-2acctpc6jH5DWL3fF5V6bKF8?usp=sharing
```