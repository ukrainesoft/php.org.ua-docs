Завантажує збережену модель SVM

-   [« SVMModel::getSvrProbability](svmmodel.getsvrprobability.html)
    
-   [SVMModel::predictprobability »](svmmodel.predict-probability.html)
    
-   [PHP Manual](index.html)
    
-   [SVMModel](class.svmmodel.html)
    
-   Завантажує збережену модель SVM
    

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

-   [SVMModel::save()](svmmodel.save.html) - Зберегти готову модель у файл