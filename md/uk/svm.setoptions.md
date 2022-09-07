---
navigation:
  - svm.getoptions.md: '« SVM::getOptions'
  - svm.train.md: 'SVM::train »'
  - index.md: PHP Manual
  - class.svm.md: SVM
title: 'SVM::setOptions'
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
