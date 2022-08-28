Конструктор класу SVMModel

-   [« SVMModel::checkProbabilityModel](svmmodel.checkprobabilitymodel.html)
    
-   [SVMModel::getLabels »](svmmodel.getlabels.html)
    
-   [PHP Manual](index.html)
    
-   [SVMModel](class.svmmodel.html)
    
-   Конструктор класу SVMModel
    

# SVMModel::construct

(PECL svm >= 0.1.0)

SVMModel::construct - Конструктор класу SVMModel

### Опис

public **SVMModel::construct**(string `$filename`

Створює об'єкт класу SVMModel. Зазвичай моделі створюються методом SVM:: train, але збережені моделі можна відновити безпосередньо.

### Список параметрів

`filename`

Ім'я файлу, у якому збережено модель.

### Помилки

Викидає виняток **SVMException** у разі виникнення помилки

### Дивіться також

-   [SVMModel::load()](svmmodel.load.html) - Завантажує збережену модель SVM