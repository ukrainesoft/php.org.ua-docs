Клас SVMModel

-   [« SVM::train](svm.train.html)
    
-   [SVMModel::checkProbabilityModel »](svmmodel.checkprobabilitymodel.html)
    
-   [PHP Manual](index.html)
    
-   [SVM](book.svm.html)
    
-   Клас SVMModel
    

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

-   [SVMModel::checkProbabilityModel](svmmodel.checkprobabilitymodel.html) — Повертає true, якщо модель містить інформацію про ймовірність
-   [SVMModel::construct](svmmodel.construct.html) - Конструктор класу SVMModel
-   [SVMModel::getLabels](svmmodel.getlabels.html) — Повертає мітки, на яких навчалася модель
-   [SVMModel::getNrClass](svmmodel.getnrclass.html) — Повертає кількість класів, для яких навчалась модель
-   [SVMModel::getSvmType](svmmodel.getsvmtype.html) - Отримати тип SVM, з яким навчалася модель
-   [SVMModel::getSvrProbability](svmmodel.getsvrprobability.html) — Отримати величину сигми для регресійного типу
-   [SVMModel::load](svmmodel.load.html) — Завантажує збережену модель SVM
-   [SVMModel::predictprobability](svmmodel.predict-probability.html) — Повертає можливість класу для заданих даних
-   [SVMModel::predict](svmmodel.predict.html) — Передбачити значення на основі нових даних
-   [SVMModel::save](svmmodel.save.html) — Зберегти готову модель у файл