---
navigation:
  - transliterator.geterrorcode.md: '« Transliterator::getErrorCode'
  - transliterator.listids.md: 'Transliterator::listIDs »'
  - index.md: PHP Manual
  - class.transliterator.md: Transliterator
title: 'Transliterator::getErrorMessage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Transliterator::getErrorMessage

# transliterator\_get\_error\_message

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::getErrorMessage -- transliterator\_get\_error\_message — Отримати останнє повідомлення про помилку

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Transliterator::getErrorMessage(): string|false
```

Процедурний стиль

```methodsynopsis
transliterator_get_error_message(Transliterator $transliterator): string|false
```

Повертає останнє повідомлення про помилку.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`transliterator`

### Значення, що повертаються

Сообщение об ошибке или\*\*`false`\*\*якщо помилок не було або якщо отримати його не вдалося.

### Дивіться також

-   [Transliterator::getErrorCode()](transliterator.geterrorcode.md) \- Отримати код останньої помилки
-   [Transliterator::listIDs()](transliterator.listids.md) \- Отримати ідентифікатори транслітератора
