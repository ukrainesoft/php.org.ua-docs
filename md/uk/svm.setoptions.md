Встановити параметри навчання

-   [« SVM::getOptions](svm.getoptions.md)
    
-   [SVM::train »](svm.train.md)
    
-   [PHP Manual](index.md)
    
-   [SVM](class.svm.md)
    
-   Встановити параметри навчання
    

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