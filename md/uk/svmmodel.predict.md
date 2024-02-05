---
navigation:
  - svmmodel.predict-probability.md: '« SVMModel::predict\_probability'
  - svmmodel.save.md: 'SVMModel::save »'
  - index.md: PHP Manual
  - class.svmmodel.md: SVMModel
title: 'SVMModel::predict'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SVMModel::predict

(PECL svm >= 0.1.0)

SVMModel::predict — Передбачити значення на основі нових даних

### Опис

```methodsynopsis
public SVMModel::predict(array $data): float
```

Функція приймає масив даних і намагається передбачити клас чи величину регресії, ґрунтуючись на моделі, навченій на попередніх даних.

### Список параметрів

`data`

Дані класифікації. Масив повинен містити елементи у форматі "ознака" => "значення", відсортований за зростанням ознаки. Ознаки не обов'язково повинні бути безперервною послідовністю.

### Значення, що повертаються

Прогнозоване значення типу float. У разі класифікації воно відображатиме мітку класу, а у разі регресії – раціональне число. У разі виникнення помилки викидає SVMException

### Дивіться також

-   [SVM::train()](svm.train.md) \- Створити SVMModel на основі навчальних даних
