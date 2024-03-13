# Homework 3
Задача: с помощью техники Self-supervised learning, разобранною на лекции, провести эксперименты 

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

## Архитектура
MobileNetV3 Large

## Гиперпараметры
* optimizer: AdamW
* lr: 0.001
* betas:  (0.9, 0.999)
* weight_decay: 0.01

## Результаты предобучения с помощью Self-supervised learning (определение номера патча относительно центра)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/9ac08089-ab4d-42ae-a6d4-fdcd89bace90)
![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/e6b8e15b-dc56-466b-9a4b-e5fffb5084cb)
![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/aec9c5e8-4c91-490d-8569-1d930633fac9)


## Эксперимент 1
1. Предобучить feature extracor вашей архитектуры на всем датасете с помощью Self-supervised learning без использования разметки
2. Использовать предобученный feature extracor в архитектуре сети для обучения на 100% размеченной выборки
3. Сравнить: 
- как быстро менялись лоссы в обучении без feature extracor (в ДЗ 1) и с предобученным feature extracor
- как быстро менялись метрики с использованием предобученного feature extracor и без
- какая из сетей достигла плато быстрее
- какие максимальные метрики

### Лоссы
Без предобучения feature extracor

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/be4d8c89-e253-462b-b96e-f9e0574c6235)

С предобучением

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/8501504b-3a1e-4ff8-b667-33bd59e55ff7)

Предобучение хоть и не помогло добиться лучшего значения лосса на валидации, но помогло быстрее выйти на плато

### Метрики 
Без предобучения feature extracor

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/6b7b7edb-5624-4d79-b6cd-ba964b5b6355)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/c3fa9dee-9d0b-4b37-9935-a16a20ad66d9)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/77b850a0-50b6-4df6-a244-bb5cf2e7fb0c)


С предобучением feature extracor

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/074183cd-af35-4d74-8aa8-139768c5faad)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/deb755d4-97ae-4486-989d-763bde57e623)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/f71c4f9c-e658-482c-abc9-3e5cf951351e)

Метрики без предобучения:
* F1 = 0.686
* Precision = 0.688
* Recall = 0.687

Метрики с предобучением:
* F1 = 0.687
* Precision = 0.694
* Recall = 0.687

Предобучение хоть и не помогло добиться лучшего значения метрик на валидации, но помогло быстрее выйти на плато


## Эксперимент 2
1. Повторить ДЗ1, используя 50% размеченной выборки
2. Предобучить feature extracor вашей архитектуры на всем датасете с помощью Self-supervised learning без использования разметки
3. Использовать предобученный feature extracor в архитектуре сети для обучения на 50% размеченной выборки
4. Сравнить: 
- как быстро менялись лоссы в обечении без feature extracor и с предобученным feature extracor
- как быстро менялись метрики с использованием предобученного feature extracor и без
- какая из сетей достигла плато быстрее
- какие максимальные метрики

### Лоссы
Без предобучения feature extracor

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/fa7dfdcc-d989-403d-8ffc-8e95ce7e99d9)

С предобучением

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/855a2185-d358-43d2-81d0-f7d97969d502)

Предобучение помогло добиться лучшего значения лосса на валидации и существенно быстрее его достигнуть

### Метрики 
Без предобучения feature extracor

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/138f2c8c-7255-424a-98fc-a3da20970382)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/ca803753-2f1a-4d4a-ae68-c37d8606cadf)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/732cfbf6-e18e-41f7-b69d-83e965237c3f)


С предобучением feature extracor

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/827d42d0-d297-4aff-9d48-a356d3d5ebb7)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/24b29af4-db90-4312-af65-c60c1a311772)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/0e7e6867-a30f-43b0-abdc-0d29787cc072)


Метрики без предобучения:
* F1 = 0.494
* Precision = 0.624
* Recall = 0.492

Метрики с предобучением:
* F1 = 0.599
* Precision = 0.603
* Recall = 0.6025

Предобучение помогло добиться лучшего значения метрик на валидации


## Эксперимент 3
1. Повторить ДЗ1, используя 10% размеченной выборки
2. Предобучить feature extracor вашей архитектуры на всем датасете с помощью Self-supervised learning без использования разметки
3. Использовать предобученный feature extracor в архитектуре сети для обучения на 10% размеченной выборки
4. Сравнить: 
- как быстро менялись лоссы в обечении без feature extracor и с предобученным feature extracor
- как быстро менялись метрики с использованием предобученного feature extracor и без
- какая из сетей достигла плато быстрее
- какие максимальные метрики

### Лоссы
Без предобучения feature extracor

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/6e0cceed-094a-4b2b-96a5-dcda0177354a)

С предобучением

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/31e5f930-8efa-4b85-866b-5be8d516f1ac)

Предобучение помогло добиться лучшего значения лосса на валидации

### Метрики 
Без предобучения feature extracor

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/3ca0b87d-f00e-4a72-853a-f83237065830)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/df7051f5-7dac-41c6-9942-0ddc1a1d1d73)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/d4f24ef4-d8bd-4c56-96c8-07ea9e3fd307)

С предобучением feature extracor

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/07c2a4fe-15cc-4967-a809-7c7d50d66c9c)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/acfbbf9e-57b8-43a4-874d-5ed21c4f9e8e)

![image](https://github.com/trew12/processing_and_generating_images_course/assets/64497667/4b540ec3-aa4e-4e9b-8dca-9c1e69e635e8)

Метрики без предобучения:
* F1 = 0.018
* Precision = 0.01
* Recall = 0.1

Метрики с предобучением:
* F1 = 0.413
* Precision = 0.431
* Recall = 0.411

Модель без предобучения не смогла никуда сойтись за заданное число итераций, а предобученная модель просто дала сниженные метрики по сравнению с обучением на большем числе данных
