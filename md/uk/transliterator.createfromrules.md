---
navigation:
  - transliterator.create.md: '« Transliterator::create'
  - transliterator.createinverse.md: 'Transliterator::createInverse »'
  - index.md: PHP Manual
  - class.transliterator.md: Transliterator
title: 'Transliterator::createFromRules'
---
# Transliterator::createFromRules

# transliteratorcreatefromrules

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::createFromRules -- transliteratorcreatefromrules - Створити транслітератор на основі правил

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

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`rules`

Правила, описані в розділі Transform Rules Syntax звіту UTS #35: Unicode LDML.

`direction`

Напрямок транслітерації. За замовчуванням [Transliterator::FORWARD](class.transliterator.html#transliterator.constants.forward). Можно використовувати [Transliterator::REVERSE](class.transliterator.html#transliterator.constants.reverse)

### Значення, що повертаються

Повертає об'єкт [Transliterator](class.transliterator.md) або **`null`** у разі виникнення помилки.

### Дивіться також

-   [Transliterator::getErrorMessage()](transliterator.geterrormessage.md) - Отримати останнє повідомлення про помилку
-   [Transliterator::create()](transliterator.create.md) - Створити транслітератор
