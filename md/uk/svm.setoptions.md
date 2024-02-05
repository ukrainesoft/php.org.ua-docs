---
navigation:
  - svm.getoptions.md: '« SVM::getOptions'
  - svm.train.md: 'SVM::train »'
  - index.md: PHP Manual
  - class.svm.md: SVM
title: 'SVM::setOptions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SVM::setOptions

(PECL svm >= 0.1.0)

SVM::setOptions — Встановити параметри навчання

### Опис

```methodsynopsis
public SVM::setOptions(array $params): bool
```

Встановлює один або декілька параметрів навчання.

### Список параметрів

`params`

Масив параметрів навчання, де як ключі використовуються константи SVM.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, у разі виникнення помилки викидає SVMException.
