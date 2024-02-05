---
navigation:
  - svmmodel.checkprobabilitymodel.md: '« SVMModel::checkProbabilityModel'
  - svmmodel.getlabels.md: 'SVMModel::getLabels »'
  - index.md: PHP Manual
  - class.svmmodel.md: SVMModel
title: 'SVMModel::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SVMModel::\_\_construct

(PECL svm >= 0.1.0)

SVMModel::\_\_construct - Конструктор класу SVMModel

### Опис

public**SVMModel::\_\_construct**(string`$filename`

Створює об'єкт класу SVMModel. Зазвичай моделі створюються методом SVM:: train, але збережені моделі можна відновити безпосередньо.

### Список параметрів

`filename`

Ім'я файлу, у якому збережено модель.

### Помилки

Викидає виняток **SVMException**в случае возникновения ошибки

### Дивіться також

-   [SVMModel::load()](svmmodel.load.md) \- Завантажує збережену модель SVM
