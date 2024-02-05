---
navigation:
  - stomp.getdetails.md: '« StompException::getDetails'
  - intro.svm.md: Вступ "
  - index.md: PHP Manual
  - refs.remote.other.md: Інші служби
title: Support Vector Machine (Додаткова векторна машина)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Support Vector Machine (Додаткова векторна машина)

-   [Вступ](intro.svm.md)
-   [Встановлення та налаштування](svm.setup.md)
    -   [Вимоги](svm.requirements.md)
    -   [Установка](svm.installation.md)
    -   [Налаштування під час виконання](svm.configuration.md)
    -   [Типи ресурсів](svm.resources.md)
-   [Приклади](svm.examples.md)
-   [SVM](class.svm.md) \- Клас SVM
    -   [SVM::\_\_construct](svm.construct.md) \- Конструктор класу SVM
    -   [SVM::crossvalidate](svm.crossvalidate.md)— Тестування навчальних параметрів на підмножинах навчальних даних
    -   [SVM::getOptions](svm.getoptions.md)— Отримати поточні параметри навчання
    -   [SVM::setOptions](svm.setoptions.md) \- Встановити параметри навчання
    -   [SVM::train](svm.train.md)— Створити SVMModel на основі навчальних даних
-   [SVMModel](class.svmmodel.md) \- Клас SVMModel
    -   [SVMModel::checkProbabilityModel](svmmodel.checkprobabilitymodel.md)— Повертає true, якщо модель містить інформацію про можливості
    -   [SVMModel::\_\_construct](svmmodel.construct.md) \- Конструктор класу SVMModel
    -   [SVMModel::getLabels](svmmodel.getlabels.md)— Повертає мітки, на яких навчалася модель
    -   [SVMModel::getNrClass](svmmodel.getnrclass.md)— Повертає кількість класів, для яких навчалась модель
    -   [SVMModel::getSvmType](svmmodel.getsvmtype.md)— Отримати тип SVM, з яким навчалася модель
    -   [SVMModel::getSvrProbability](svmmodel.getsvrprobability.md)— Отримати величину сигми для регресійного типу
    -   [SVMModel::load](svmmodel.load.md)— Завантажує збережену модель SVM
    -   [SVMModel::predict\_probability](svmmodel.predict-probability.md)— Повертає можливість класу для заданих даних
    -   [SVMModel::predict](svmmodel.predict.md)— Передбачити значення на основі нових даних
    -   [SVMModel::save](svmmodel.save.md)— Зберегти готову модель у файл
