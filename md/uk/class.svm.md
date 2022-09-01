---
navigation:
  - svm.examples.md: « Приклади
  - svm.construct.md: 'SVM::construct »'
  - index.md: PHP Manual
  - book.svm.md: SVM
title: Клас SVM
---
# Клас SVM

(PECL svm >= 0.1.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class SVM
     
     {
    
    /* Константы */
    
     const
     int
      C_SVC = 0;

    const
     int
      NU_SVC = 1;

    const
     int
      ONE_CLASS = 2;

    const
     int
      EPSILON_SVR = 3;

    const
     int
      NU_SVR = 4;

    const
     int
      KERNEL_LINEAR = 0;

    const
     int
      KERNEL_POLY = 1;

    const
     int
      KERNEL_RBF = 2;

    const
     int
      KERNEL_SIGMOID = 3;

    const
     int
      KERNEL_PRECOMPUTED = 4;

    const
     int
      OPT_TYPE = 101;

    const
     int
      OPT_KERNEL_TYPE = 102;

    const
     int
      OPT_DEGREE = 103;

    const
     int
      OPT_SHRINKING = 104;

    const
     int
      OPT_PROPABILITY = 105;

    const
     int
      OPT_GAMMA = 201;

    const
     int
      OPT_NU = 202;

    const
     int
      OPT_EPS = 203;

    const
     int
      OPT_P = 204;

    const
     int
      OPT_COEF_ZERO = 205;

    const
     int
      OPT_C = 206;

    const
     int
      OPT_CACHE_SIZE = 207;


    /* Методы */
    
   public __construct()

    public svm::crossvalidate(array $problem, int $number_of_folds): float
public getOptions(): array
public setOptions(array $params): bool
public svm::train(array $problem, array $weights = ?): SVMModel

   }
```

## Обумовлені константи

## Константи SVM

**`SVM::C_SVC`**

Базовий тип SVM. Тип за замовчуванням, добрий для початку.

**`SVM::NU_SVC`**

Тип NUSVC використовує інший, більш гнучкий підхід до розважування помилок.

**`SVM::ONE_CLASS`**

Однокласова модель. Тренує тільки на одному класі, використовуючи "випадають" дані як негативні приклади

**`SVM::EPSILON_SVR`**

Тип для регресії (прогнозування значення, а не класу)

**`SVM::NU_SVR`**

Тип регресії SVM у стилі NU

**`SVM::KERNEL_LINEAR`**

Дуже просте ядро, яке добре працює для класифікації проблем великих документів

**`SVM::KERNEL_POLY`**

Поліномінальне ядро

**`SVM::KERNEL_RBF`**

Стандартне Гаусове RBD ядро. Добре обробляє нелінійні проблеми та є добрим значенням за умовчанням для класифікації

**`SVM::KERNEL_SIGMOID`**

Ядро, що базується на сигмоїдній функції. Дуже схоже використання дворівневої сигмоїдної нейронної мережі

**`SVM::KERNEL_PRECOMPUTED`**

Попередньо обчислене ядро ​​– зараз не підтримується

**`SVM::OPT_TYPE`**

Опціональний ключ типу SVM

**`SVM::OPT_KERNEL_TYPE`**

Опціональний ключ типу ядра

**`SVM::OPT_DEGREE`**

**`SVM::OPT_SHRINKING`**

Параметр навчання, логічне значення, що визначає використання скорочувальної евристики

**`SVM::OPT_PROBABILITY`**

Параметр навчання, логічне значення, що визначає, чи збиратимуться і використовуватимуться оцінки ймовірності

**`SVM::OPT_GAMMA`**

Параметр алгоритму для наступних типів ядра: Поліномінальне, RBF та Сігмоїдне

**`SVM::OPT_NU`**

Опціональний ключ параметра nu. Використовується лише з типами NU SVM

**`SVM::OPT_EPS`**

Опціональний ключ для Epsilon. Використовується тільки в Епсілон-регресії

**`SVM::OPT_P`**

Навчальний параметр для Епсилон-регресії SVR

**`SVM::OPT_COEF_ZERO`**

Параметр алгоритму для поліномінального та сигмоїдного ядра

**`SVM::OPT_C`**

Опція для параметра вартості, що контролює компроміс між помилками та невизначеності - фактично штраф за помилкову класифікацію навчальних прикладів.

**`SVM::OPT_CACHE_SIZE`**

Розмір кешу в пам'яті у мегабайтах

## Зміст

-   [SVM::construct](svm.construct.md) - Конструктор класу SVM
-   [SVM::crossvalidate](svm.crossvalidate.md) — Тестування навчальних параметрів на підмножинах навчальних даних
-   [SVM::getOptions](svm.getoptions.md) — Отримати поточні параметри навчання
-   [SVM::setOptions](svm.setoptions.md) - Встановити параметри навчання
-   [SVM::train](svm.train.md) — Створити SVMModel на основі навчальних даних
