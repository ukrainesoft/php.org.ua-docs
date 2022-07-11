- [« Приклади](svm.examples.md)
- [SVM::\_\_construct »](svm.construct.md)

- [PHP Manual](index.md)
- [SVM](book.svm.md)
- Клас SVM

# Клас SVM

(PECL svm \>= 0.1.0)

## Вступ

## Огляд класів

class **SVM** {

/\* Константи \*/

const int `C_SVC` = 0;

const int `NU_SVC` = 1;

const int `ONE_CLASS` = 2;

const int `EPSILON_SVR` = 3;

const int `NU_SVR` = 4;

const int `KERNEL_LINEAR` = 0;

const int `KERNEL_POLY` = 1;

const int `KERNEL_RBF` = 2;

const int `KERNEL_SIGMOID` = 3;

const int `KERNEL_PRECOMPUTED` = 4;

const int `OPT_TYPE` = 101;

const int `OPT_KERNEL_TYPE` = 102;

const int `OPT_DEGREE` = 103;

const int `OPT_SHRINKING` = 104;

const int `OPT_PROPABILITY` = 105;

const int `OPT_GAMMA` = 201;

const int `OPT_NU` = 202;

const int `OPT_EPS` = 203;

const int `OPT_P` = 204;

const int `OPT_COEF_ZERO` = 205;

const int `OPT_C` = 206;

const int `OPT_CACHE_SIZE` = 207;

/\* Методи \*/

public [\_\_construct](svm.construct.md)()

public [svm::crossvalidate](svm.crossvalidate.md)(array `$problem`,
int `$number_of_folds`): float

public [getOptions](svm.getoptions.md)(): array

public [setOptions](svm.setoptions.md)(array `$params`): bool

public [svm::train](svm.train.md)(array `$problem`, array `$weights` =
?): [SVMModel](class.svmmodel.md)

}

## Зумовлені константи

## Константи SVM

**`SVM::C_SVC`**
Базовий тип SVM. Тип за замовчуванням, добрий для початку.

**`SVM::NU_SVC`**
Тип NU_SVC використовує інший, більш гнучкий підхід до розважування помилок.

**`SVM::ONE_CLASS`**
Однокласова модель. Тренує лише на одному класі, використовуючи
"випадають" дані як негативні приклади

**`SVM::EPSILON_SVR`**
Тип для регресії (прогнозування значення, а не класу)

**`SVM::NU_SVR`**
Тип регресії SVM у стилі NU

**`SVM::KERNEL_LINEAR`**
Дуже просте ядро, яке добре працює для класифікації проблем
великих документів

**`SVM::KERNEL_POLY`**
Поліномінальне ядро

**`SVM::KERNEL_RBF`**
Стандартне Гаусове RBD ядро. Добре обробляє нелінійні проблеми та
є добрим значенням за умовчанням для класифікації

**`SVM::KERNEL_SIGMOID`**
Ядро, що базується на сигмоїдній функції. Дуже схоже на використання
дворівневої сигмоїдної нейронної мережі

**`SVM::KERNEL_PRECOMPUTED`**
Попередньо обчислене ядро – зараз не підтримується

**`SVM::OPT_TYPE`**
Опціональний ключ типу SVM

**`SVM::OPT_KERNEL_TYPE`**
Опціональний ключ типу ядра

**`SVM::OPT_DEGREE`**

**`SVM::OPT_SHRINKING`**
Параметр навчання, логічне значення, що визначає використання
скорочує евристики

**`SVM::OPT_PROBABILITY`**
Параметр навчання, логічне значення, що визначає, чи будуть
збиратися та використовуватися оцінки ймовірності

**`SVM::OPT_GAMMA`**
Параметр алгоритму для наступних типів ядра: Поліномінальний, RBF та
Сигмоїдне

**`SVM::OPT_NU`**
Опціональний ключ параметра nu. Використовується лише з типами NU\_
SVM

**`SVM::OPT_EPS`**
Опціональний ключ для Epsilon. Використовується тільки в
Епсилон-регресії

**`SVM::OPT_P`**
Навчальний параметр для Епсілон-регресії SVR

**`SVM::OPT_COEF_ZERO`**
Параметр алгоритму для поліномінального та сигмоїдного ядра

**`SVM::OPT_C`**
Опція параметра вартості, що контролює компроміс між помилками
та невизначеності - фактично штраф за помилкову класифікацію
навчальних прикладів.

**`SVM::OPT_CACHE_SIZE`**
Розмір кешу в пам'яті у мегабайтах

## Зміст

- [SVM::\_\_construct](svm.construct.md) - Конструктор класу SVM
- [SVM::crossvalidate](svm.crossvalidate.md) — Тестування
навчальних параметрів на підмножинах навчальних даних
- [SVM::getOptions](svm.getoptions.md) — Отримати поточні установки
навчання
- [SVM::setOptions](svm.setoptions.md) — Встановити установки
навчання
- [SVM::train](svm.train.md) — Створити SVMModel на основі учнів
даних
