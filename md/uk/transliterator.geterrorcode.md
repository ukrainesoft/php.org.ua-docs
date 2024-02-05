---
navigation:
  - transliterator.createinverse.md: '« Transliterator::createInverse'
  - transliterator.geterrormessage.md: 'Transliterator::getErrorMessage »'
  - index.md: PHP Manual
  - class.transliterator.md: Transliterator
title: 'Transliterator::getErrorCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Transliterator::getErrorCode

# transliterator\_get\_error\_code

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::getErrorCode -- transliterator\_get\_error\_code — Отримати код останньої помилки

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Transliterator::getErrorCode(): int|false
```

Процедурний стиль

```methodsynopsis
transliterator_get_error_code(Transliterator $transliterator): int|false
```

Повертає код останньої помилки.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`transliterator`

### Значення, що повертаються

Код ошибки или\*\*`false`\*\*якщо помилок не було або якщо отримати його не вдалося.

### Дивіться також

-   [Transliterator::getErrorMessage()](transliterator.geterrormessage.md) \- Отримати останнє повідомлення про помилку
-   [Transliterator::listIDs()](transliterator.listids.md) \- Отримати ідентифікатори транслітератора
