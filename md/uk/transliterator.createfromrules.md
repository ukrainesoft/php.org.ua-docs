---
navigation:
  - transliterator.create.md: '« Transliterator::create'
  - transliterator.createinverse.md: 'Transliterator::createInverse »'
  - index.md: PHP Manual
  - class.transliterator.md: Transliterator
title: 'Transliterator::createFromRules'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Transliterator::createFromRules

# transliterator\_create\_from\_rules

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::createFromRules -- transliterator\_create\_from\_rules - Створити транслітератор на основі правил

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Transliterator::createFromRules(string $rules, int $direction = Transliterator::FORWARD): ?Transliterator
```

Процедурний стиль

```methodsynopsis
transliterator_create_from_rules(string $rules, int $direction = Transliterator::FORWARD): ?Transliterator
```

Створити транслітератор з урахуванням правил.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`rules`

Правила, описані в розділі Transform Rules Syntax звіту UTS #35: Unicode LDML.

`direction`

Направление транслитерации. По умолчанию[Transliterator::FORWARD](class.transliterator.md#transliterator.constants.forward). Можна використовувати [Transliterator::REVERSE](class.transliterator.md#transliterator.constants.reverse)

### Значення, що повертаються

Повертає об'єкт [Transliterator](class.transliterator.md)или\*\*`null`\*\*в случае возникновения ошибки.

### Дивіться також

-   [Transliterator::getErrorMessage()](transliterator.geterrormessage.md) \- Отримати останнє повідомлення про помилку
-   [Transliterator::create()](transliterator.create.md) \- Створити транслітератор
