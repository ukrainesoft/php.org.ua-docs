---
navigation:
  - svm.train.md: '« SVM::train'
  - svmmodel.checkprobabilitymodel.md: 'SVMModel::checkProbabilityModel »'
  - index.md: PHP Manual
  - book.svm.md: SVM
title: Клас SVMModel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SVMModel

(PECL svm >= 0.1.0)

## Вступ

SVMModel – це кінцевий результат процесу навчання. Він може бути використаний для класифікації невідомих даних.

## Огляд класів

```classsynopsis


    
    
     
      class SVMModel
     
     {
    

    /* Методы */
    
   public __construct(string $filename = ?)

    public checkProbabilityModel(): bool
public getLabels(): array
public getNrClass(): int
public getSvmType(): int
public getSvrProbability(): float
public load(string $filename): bool
public predict_probability(array $data): float
public predict(array $data): float
public save(string $filename): bool

   }
```

## Зміст

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
