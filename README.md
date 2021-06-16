# E2A7_1

## Changes Made  
- Migrated code to PyTorchLightning
- Used Torchmetrics library for Accuracy

## Loading Data

As required by the instructions, only the .txt files in the zip have been used (unlike previously where the `pytreebank` module was used).

## Explanation of Files

**`sentiment_labels.txt`:** This file contains the mapping of phrase ids (not the phrases) to the sentiments. The `pd.cut` method was used to categorize them into 5 discrete classes. The 'sentiments' are henceforth referred as 'labels'

**`datasetSentences.txt`:** This file contains the sentences without any sentiments

**`dictionary.txt`:** This file contains the mapping of phrases to their sentiments. After this file is loaded, the phrases are mapped to the sentences, followed by mapping to the (discrete) labels.

**`datasetSplit.txt`:** This file contains the splitting of the dataset into train/test/dev set. Since we are only required to have a train/test split, this file is NOT used

Using regular expressions, the sentences are 'cleaned'. Only these cleaned sentences and their labels are retained and other columns are dropped

The final dataset has 11286 samples.

## Data Split
The data is split into train/test  sets using a 70/30 ratio.

## Model
Almost the same model as presented in the orginal notebooks was used. 



## Results

I was able to get >>60% on the train dataset. Despite tinkering with the hyperparameters, I wasn't able to get accuracy > 40% in the validation dataset.

#### Training Log
|    epoch    |   Train Acc |  Train Loss |   Valid Acc |  Valid Loss |
| ----------- | ----------- | ----------- | ----------- | ----------- | 
|           1 |       26.38 |      1.5746 |      30.018 |      1.5603 |
|           2 |      30.886 |      1.5308 |      32.487 |        1.51 |
|           3 |      37.709 |      1.4197 |      34.879 |      1.4888 |
|           4 |       44.81 |      1.2915 |      36.799 |      1.4885 |
|           5 |      50.962 |      1.1527 |       34.82 |       1.562 |
|           6 |      57.532 |      1.0284 |      36.031 |      1.6687 |
|           7 |      63.532 |     0.90568 |      35.204 |        1.85 |
|           8 |      68.924 |     0.80161 |      35.145 |      1.9615 |
|           9 |      73.595 |     0.70365 |      34.495 |      2.1086 |
|          10 |      77.354 |     0.62018 |      35.263 |      2.1964 |
|          11 |      80.241 |     0.55864 |       34.79 |      2.3029 |
|          12 |      83.038 |     0.49319 |      34.672 |      2.4138 |
|          13 |      85.848 |     0.43099 |      35.351 |      2.5511 |
|          14 |      86.911 |     0.38719 |      33.579 |      2.6121 |
|          15 |      88.481 |     0.35891 |      34.997 |      2.7361 |
|          16 |      89.418 |     0.32695 |      34.406 |      2.8067 |
|          17 |      91.025 |     0.29164 |      34.702 |      2.8948 |
|          18 |      91.797 |     0.26694 |      34.377 |      2.9899 |
|          19 |      92.253 |     0.25037 |      34.584 |      3.0636 |
|          20 |      92.962 |     0.22841 |      34.584 |      3.0698 |

#### Confusion Matrix
![Confusion Matrix](cm.png?raw=true "Backpropagation in Excels")

#### Loss/Accuracy vs Epochs
![Alt text](logs.png?raw=true "Backpropagation in Excels")


## Sample outcomes


![samples](samples.png?raw=true "Backpropagation in Excels")

