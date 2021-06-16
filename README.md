# E2A7_1

## Changes Made  
- Migrated code to PyTorchLightning
- Used Torchmetrics library for Accuracy

## Loading Data

As required by the instructions, only the .txt files in the zip have been used (unlike previously where the `pytreebank` module was used).

## Model
Almost the same model as presented in the orginal notebooks was used. 



## Results

I was able to get >>60% on the train dataset. Despite tinkering with the hyperparameters, I wasn't able to get accuracy > 40% in the validation dataset.

#### Training Log
|    epoch    |   Train Acc |  Train Loss |   Valid Acc |  Valid Loss |
| ----------- | ----------- | ----------- | ----------- | ----------- | 
|           1 |       26.38 |      1.5746 |      29.959 |      1.5603 |
|           2 |      30.937 |      1.5308 |      32.546 |      1.5099 |
|           3 |      37.785 |      1.4196 |      34.849 |      1.4888 |
|           4 |      44.772 |      1.2915 |      36.799 |      1.4882 |
|           5 |      50.911 |      1.1527 |       34.79 |      1.5626 |
|           6 |      57.418 |      1.0284 |       36.06 |      1.6678 |
|           7 |      63.481 |     0.90592 |      35.145 |      1.8482 |
|           8 |      68.848 |     0.80195 |      35.145 |      1.9479 |
|           9 |      73.684 |     0.70367 |      34.318 |      2.1228 |
|          10 |      77.304 |     0.62305 |      34.702 |      2.2082 |
|          11 |      79.734 |     0.56275 |      34.584 |      2.2721 |
|          12 |      83.101 |     0.49089 |      34.111 |      2.4232 |
|          13 |       85.38 |     0.43914 |       34.79 |      2.5672 |
|          14 |      86.494 |     0.39876 |        34.2 |      2.6014 |
|          15 |      88.304 |      0.3604 |      35.027 |      2.7519 |
|          16 |      89.899 |     0.31924 |      34.111 |      2.8246 |
|          17 |      90.911 |     0.28823 |      34.082 |      2.8982 |
|          18 |      91.418 |     0.27154 |      33.786 |      2.9746 |
|          19 |       92.43 |      0.2495 |      33.373 |       3.066 |
|          20 |      92.658 |     0.23752 |      34.672 |      3.0495 |

#### Confusion Matrix
![Confusion Matrix](cm.png?raw=true "Backpropagation in Excels")

#### Loss/Accuracy vs Epochs
![Alt text](logs.png?raw=true "Backpropagation in Excels")


## Sample outcomes


![samples](samples.png?raw=true "Backpropagation in Excels")

