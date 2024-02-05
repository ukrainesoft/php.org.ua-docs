---
navigation:
  - intldateformatter.settimezone.md: '« IntlDateFormatter::setTimeZone'
  - resourcebundle.count.md: 'ResourceBundle::count »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас ResourceBundle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ResourceBundle

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 2.0.0)

## Вступ

Локалізовані програмні продукти часто потребують наборів даних, підготовлених залежно від поточної локалі, наприклад: повідомлення, мітки, шаблони форматування. Механізм ресурсів ICU дозволяє задати набори ресурсів, які програма може завантажити в залежності від поточної локалі та використовувати уніфікованим, не залежним від локалі, способом.

Цей клас реалізує доступ до файлів ресурсів ICU. Ці файли є бінарними масивами даних, які використовує ICU для зберігання локалізованих даних.

Пакет ресурсів ICU може містити прості та складні ресурси. Складні ресурси - це контейнери, які можуть бути індексовані як числами, так і рядками (аналогічно масивам PHP). Прості ресурси можуть бути наступних типів: рядки, цілі, бінарні поля даних та цілочисленні масиви.

**ResourceBundle**підтримує прямий доступ до даних через синтаксис доступу до масивів та ітеруватися через [foreach](control-structures.foreach.md), як і і через методи. В результаті буде отримано значення PHP для простих ресурсів та об'єкти **ResourceBundle** для складних. Усі ресурси доступні лише для читання.

## Огляд класів

```classsynopsis

    
     class ResourceBundle
    

    
     implements
      IteratorAggregate,

     Countable {

    /* Методы */
    
   public __construct(?string $locale, ?string $bundle, bool $fallback = true)

    public count(): int
public static create(?string $locale, ?string $bundle, bool $fallback = true): ?ResourceBundle
public getErrorCode(): int
public getErrorMessage(): string
public get(string|int $index, bool $fallback = true): mixed
public static getLocales(string $bundle): array|false

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Класс**ResourceBundle** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.md). . Раніше було реалізовано інтерфейс [Traversable](class.traversable.md) |
| 7.4.0 | Класс**ResourceBundle** тепер реалізує інтерфейс [Countable](class.countable.md) |

## Дивіться також

-   [»  Менеджер ресурсів ICU](https://unicode-org.github.io/icu/userguide/locale/resources.md)
-   [» Дані ICU](https://unicode-org.github.io/icu/userguide/icu_data/)

## Зміст

-   [ResourceBundle::count](resourcebundle.count.md)— Отримати кількість елементів у пакеті
-   [ResourceBundle::create](resourcebundle.create.md) \- Створити пакет ресурсів
-   [ResourceBundle::getErrorCode](resourcebundle.geterrorcode.md)— Отримати останній код помилки пакета
-   [ResourceBundle::getErrorMessage](resourcebundle.geterrormessage.md)— Отримати останнє повідомлення про помилку пакета
-   [ResourceBundle::get](resourcebundle.get.md)— Отримати дані з пакета
-   [ResourceBundle::getLocales](resourcebundle.locales.md)— Отримати підтримувані локалі
