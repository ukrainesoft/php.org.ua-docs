Зберегти готову модель у файл

-   [« SVMModel::predict](svmmodel.predict.html)
    
-   [SVN »](book.svn.html)
    
-   [PHP Manual](index.html)
    
-   [SVMModel](class.svmmodel.html)
    
-   Зберегти готову модель у файл
    

# SVMModel::save

(PECL svm >= 0.1.0)

SVMModel::save — Зберегти готову модель у файл

### Опис

```methodsynopsis
public SVMModel::save(string $filename): bool
```

Зберігає готову модель файлу.

### Список параметрів

`filename`

Ім'я файлу для збереження моделі.

### Значення, що повертаються

У разі виникнення помилки викидає SVMException. У разі успішного виконання повертає **`true`**

### Дивіться також

-   [SVMModel::load()](svmmodel.load.html) - Завантажує збережену модель SVM