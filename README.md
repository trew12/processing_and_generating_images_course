# Homework 1
Задача: многоклассовая классиикация

## Классы
* airplane
* automobile
* bird
* cat
* deer
* dog
* frog
* horse
* ship
* truck

## Результаты:
![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/42638cb1-fbe4-4ec6-85de-b6d912c6190f)


## Архитектура
EfficientNet-B4 

## Гиперпараметры
* optimizer: AdamW
* lr: 0.001
* betas:  (0.9, 0.999)
* weight_decay: 0.01

## CrossEntropyLoss

![CrossEntropyLoss](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/0a6c312e-7635-4400-a9af-5bf8390df333)

## F1Score

Total:

![F1Score](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/ffbd0573-150a-4bae-80e1-88fda93d2185)

By class:

![F1ScoreByClass](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/f668cb53-422e-43c9-a354-c408c4446e42)
|                | **airplane** | **automobile** | **bird** | **cat** | **deer** | **dog** | **frog** | **horse** | **ship** | **truck** |
|----------------|:------------:|:--------------:|:--------:|:-------:|:--------:|:-------:|:--------:|:---------:|:--------:|:---------:|
|    **Train**   | 0.936        | 0.961          | 0.907    | 0.857   | 0.907    | 0.882   | 0.928    | 0.941     | 0.955    | 0.953     |
| **Validation** | 0.780         | 0.852          | 0.654    | 0.537   | 0.683    | 0.634   | 0.766    | 0.777     | 0.846    | 0.804     |

## Precision
Total:

![Precision](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/35227eb2-3bcf-40e2-aa8d-60ebcc8380d0)

By class:

![PrecisionByClass](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/3a45f337-54cd-4a19-8dda-b1f778fd1cc4)


## Recall
Total:

![Recall](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/37aa2d1d-0591-4ad7-86c8-17245b400031)

By class:

![RecallByClass](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/1cfcebe3-c310-4499-9760-dc00487ef08b)




