---
navigation:
  - transliterator.construct.md: '« Transliterator::\_\_construct'
  - transliterator.createfromrules.md: 'Transliterator::createFromRules »'
  - index.md: PHP Manual
  - class.transliterator.md: Transliterator
title: 'Transliterator::create'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Transliterator::create

# transliterator\_create

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::create -- transliterator\_create — Створити транслітератор

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Transliterator::create(string $id, int $direction = Transliterator::FORWARD): ?Transliterator
```

Процедурний стиль

```methodsynopsis
transliterator_create(string $id, int $direction = Transliterator::FORWARD): ?Transliterator
```

Відкриває об'єкт Transliterator за ідентифікатором.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`id`

Ідентифікатор. Список усіх зареєстрованих ідентифікаторів транслітератора можна отримати за допомогою [Transliterator::listIDs()](transliterator.listids.md)

`direction`

Направление транслитерации. По умолчанию[\>Transliterator::FORWARD](class.transliterator.md#transliterator.constants.forward). Можна використовувати [Transliterator::REVERSE](class.transliterator.md#transliterator.constants.reverse)

### Значення, що повертаються

Повертає об'єкт [Transliterator](class.transliterator.md)или\*\*`null`\*\*в случае возникновения ошибки.

### Дивіться також

-   [Transliterator::getErrorMessage()](transliterator.geterrormessage.md) \- Отримати останнє повідомлення про помилку
-   [Transliterator::\_\_construct()](transliterator.construct.md) \- Приватний конструктор
