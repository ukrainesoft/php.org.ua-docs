---
navigation:
  - transliterator.geterrorcode.md: '« Transliterator::getErrorCode'
  - transliterator.listids.md: 'Transliterator::listIDs »'
  - index.md: PHP Manual
  - class.transliterator.md: Transliterator
title: 'Transliterator::getErrorMessage'
---
# Transliterator::getErrorMessage

# transliteratorgeterrormessage

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::getErrorMessage -- transliteratorgeterrormessage — Отримати останнє повідомлення про помилку

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

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`transliterator`

### Значення, що повертаються

Повідомлення про помилку або \*\*`false`\*\*якщо помилок не було або якщо отримати його не вдалося.

### Дивіться також

-   [Transliterator::getErrorCode()](transliterator.geterrorcode.md) - Отримати код останньої помилки
-   [Transliterator::listIDs()](transliterator.listids.md) - Отримати ідентифікатори транслітератора
