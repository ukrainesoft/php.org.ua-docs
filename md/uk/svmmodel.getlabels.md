---
navigation:
  - svmmodel.construct.md: '« SVMModel::\_\_construct'
  - svmmodel.getnrclass.md: 'SVMModel::getNrClass »'
  - index.md: PHP Manual
  - class.svmmodel.md: SVMModel
title: 'SVMModel::getLabels'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SVMModel::getLabels

(PECL svm >= 0.1.5)

SVMModel::getLabels — Повертає позначки, на яких навчалася модель

### Опис

```methodsynopsis
public SVMModel::getLabels(): array
```

Повертає масив міток (класів), на яких була навчена модель. Для регресивної та однокласової моделі повертається порожній масив.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив міток

### Дивіться також

-   [SVMModel::getNrClass()](svmmodel.getnrclass.md) \- Повертає кількість класів, для яких навчалась модель
