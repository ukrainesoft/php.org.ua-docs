---
navigation:
  - transliterator.createfromrules.md: '« Transliterator::createFromRules'
  - transliterator.geterrorcode.md: 'Transliterator::getErrorCode »'
  - index.md: PHP Manual
  - class.transliterator.md: Transliterator
title: 'Transliterator::createInverse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Transliterator::createInverse

# transliterator\_create\_inverse

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::createInverse -- transliterator\_create\_inverse — Створити інвертований транслітератор

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Transliterator::createInverse(): ?Transliterator
```

Процедурний стиль

```methodsynopsis
transliterator_create_inverse(Transliterator $transliterator): ?Transliterator
```

Відкриває інвертований транслітератор.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [Transliterator](class.transliterator.md)или\*\*`null`\*\*в случае возникновения ошибки.

### Дивіться також

-   [Transliterator::getErrorMessage()](transliterator.geterrormessage.md) \- Отримати останнє повідомлення про помилку
-   [Transliterator::create()](transliterator.create.md) \- Створити транслітератор
