Повертає мітки, на яких навчалася модель

-   [« SVMModel::\_\_construct](svmmodel.construct.html)
    
-   [SVMModel::getNrClass »](svmmodel.getnrclass.html)
    
-   [PHP Manual](index.html)
    
-   [SVMModel](class.svmmodel.html)
    
-   Повертає мітки, на яких навчалася модель
    

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

-   [SVMModel::getNrClass()](svmmodel.getnrclass.html) - Повертає кількість класів, для яких навчалась модель