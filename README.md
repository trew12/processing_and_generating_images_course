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
MobileNetV3 Large

## Гиперпараметры
* optimizer: AdamW
* lr: 0.001
* betas:  (0.9, 0.999)
* weight_decay: 0.01

## CrossEntropyLoss

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/08fd97cb-7f65-411a-8b6d-1cc8febcc897)


## F1Score

Total:

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/a1a3ec87-8025-48d1-a3af-d750bc1246cf)


By class:

|                | **airplane** | **automobile** | **bird** | **cat** | **deer** | **dog** | **frog** | **horse** | **ship** | **truck** |
|----------------|:------------:|:--------------:|:--------:|:-------:|:--------:|:-------:|:--------:|:---------:|:--------:|:---------:|
|    **Train**   |0.814|0.876|0.711|0.593|0.719|0.664|0.81|0.815|0.872|0.844|
| **Validation** |0.733|0.803|0.583|0.479|0.635|0.577|0.758|0.727|0.808|0.755|

## Precision
Total:

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/05023f51-638f-4f64-8335-66661711e500)


By class:

|                | **airplane** | **automobile** | **bird** | **cat** | **deer** | **dog** | **frog** | **horse** | **ship** | **truck** |
|----------------|:------------:|:--------------:|:--------:|:-------:|:--------:|:-------:|:--------:|:---------:|:--------:|:---------:|
|    **Train**   |0.812|0.877|0.723|0.596|0.702|0.675|0.801|0.824|0.867|0.841|
| **Validation** |0.738|0.802|0.651|0.489|0.705|0.54|0.729|0.701|0.823|0.705 |


## Recall
Total:

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/dc54048a-1663-4d5f-80cc-0087562cc147)


By class:

|                | **airplane** | **automobile** | **bird** | **cat** | **deer** | **dog** | **frog** | **horse** | **ship** | **truck** |
|----------------|:------------:|:--------------:|:--------:|:-------:|:--------:|:-------:|:--------:|:---------:|:--------:|:---------:|
|    **Train**   |0.816|0.874|0.699|0.59|0.737|0.653|0.82|0.807|0.878|0.847|
| **Validation** |0.728|0.803|0.527|0.47|0.577|0.62|0.789|0.754|0.793|0.814|




