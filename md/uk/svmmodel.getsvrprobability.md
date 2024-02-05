---
navigation:
  - svmmodel.getsvmtype.md: '« SVMModel::getSvmType'
  - svmmodel.load.md: 'SVMModel::load »'
  - index.md: PHP Manual
  - class.svmmodel.md: SVMModel
title: 'SVMModel::getSvrProbability'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SVMModel::getSvrProbability

(PECL svm >= 0.1.5)

SVMModel::getSvrProbability — Отримати величину сигми для регресійного типу

### Опис

```methodsynopsis
public SVMModel::getSvrProbability(): float
```

Повертає значення сигми для регресійних моделей. Якщо інформація відсутня або модель не SVR, то поверне 0.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає величину сигми
