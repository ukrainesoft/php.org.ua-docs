---
navigation:
  - svmmodel.checkprobabilitymodel.md: '« SVMModel::checkProbabilityModel'
  - svmmodel.getlabels.md: 'SVMModel::getLabels »'
  - index.md: PHP Manual
  - class.svmmodel.md: SVMModel
title: 'SVMModel::construct'
---
# SVMModel::construct

(PECL svm >= 0.1.0)

SVMModel::construct - Конструктор класу SVMModel

### Опис

public **SVMModel::construct**(string `$filename`

Створює об'єкт класу SVMModel. Зазвичай моделі створюються методом SVM:: train, але збережені моделі можна відновити безпосередньо.

### Список параметрів

`filename`

Ім'я файлу, у якому збережено модель.

### Помилки

Викидає виняток **SVMException** у разі виникнення помилки

### Дивіться також

-   [SVMModel::load()](svmmodel.load.md) - Завантажує збережену модель SVM
