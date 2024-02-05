---
navigation:
  - svmmodel.getsvrprobability.md: '« SVMModel::getSvrProbability'
  - svmmodel.predict-probability.md: 'SVMModel::predict\_probability »'
  - index.md: PHP Manual
  - class.svmmodel.md: SVMModel
title: 'SVMModel::load'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SVMModel::load

(PECL svm >= 0.1.00.1.0)

SVMModel::load — Завантажує збережену модель SVM

### Опис

```methodsynopsis
public SVMModel::load(string $filename): bool
```

Завантажує збережену модель SVM із файлу, готову до класифікації та регресу.

### Список параметрів

`filename`

Ім'я файлу для завантаження.

### Значення, що повертаються

У разі виникнення помилки викидає SVMException. У разі успішного виконання повертає **`true`**

### Дивіться також

-   [SVMModel::save()](svmmodel.save.md) \- Зберегти готову модель у файл
