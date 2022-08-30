Support Vector Machine (Додаткова векторна машина)

-   [« StompException::getDetails](stomp.getdetails.md)
    
-   [Введение »](intro.svm.md)
    
-   [PHP Manual](index.md)
    
-   [Інші служби](refs.remote.other.md)
    
-   Support Vector Machine (Додаткова векторна машина)
    

# Support Vector Machine (Додаткова векторна машина)

-   [Введение](intro.svm.md)
-   [Встановлення та налаштування](svm.setup.md)
    -   [Вимоги](svm.requirements.md)
    -   [Установка](svm.installation.md)
    -   [Налаштування під час виконання](svm.configuration.md)
    -   [Типи ресурсів](svm.resources.md)
-   [Приклади](svm.examples.md)
-   [SVM](class.svm.md) - Клас SVM
    -   [SVM::construct](svm.construct.md) - Конструктор класу SVM
    -   [SVM::crossvalidate](svm.crossvalidate.md) — Тестування навчальних параметрів на підмножинах навчальних даних
    -   [SVM::getOptions](svm.getoptions.md) — Отримати поточні параметри навчання
    -   [SVM::setOptions](svm.setoptions.md) - Встановити параметри навчання
    -   [SVM::train](svm.train.md) — Створити SVMModel на основі навчальних даних
-   [SVMModel](class.svmmodel.md) - Клас SVMModel
    -   [SVMModel::checkProbabilityModel](svmmodel.checkprobabilitymodel.md) — Повертає true, якщо модель містить інформацію про ймовірність
    -   [SVMModel::construct](svmmodel.construct.md) - Конструктор класу SVMModel
    -   [SVMModel::getLabels](svmmodel.getlabels.md) — Повертає мітки, на яких навчалася модель
    -   [SVMModel::getNrClass](svmmodel.getnrclass.md) — Повертає кількість класів, для яких навчалась модель
    -   [SVMModel::getSvmType](svmmodel.getsvmtype.md) - Отримати тип SVM, з яким навчалася модель
    -   [SVMModel::getSvrProbability](svmmodel.getsvrprobability.md) — Отримати величину сигми для регресійного типу
    -   [SVMModel::load](svmmodel.load.md) — Завантажує збережену модель SVM
    -   [SVMModel::predictprobability](svmmodel.predict-probability.html) — Повертає можливість класу для заданих даних
    -   [SVMModel::predict](svmmodel.predict.md) — Передбачити значення на основі нових даних
    -   [SVMModel::save](svmmodel.save.md) — Зберегти готову модель у файл