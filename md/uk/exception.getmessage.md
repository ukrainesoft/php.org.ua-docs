---
navigation:
  - exception.construct.md: '« Exception::construct'
  - exception.getprevious.md: 'Exception::getPrevious »'
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::getMessage'
---
# Exception::getMessage

(PHP 5, PHP 7, PHP 8)

Exception::getMessage — Отримує повідомлення про виключення

### Опис

```methodsynopsis
final public Exception::getMessage(): string
```

Повертає повідомлення виключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення виключення у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **Exception::getMessage()****

```php
<?php
try {
    throw new Exception("Какое-нибудь сообщение об ошибке");
} catch(Exception $e) {
    echo $e->getMessage();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Какое-нибудь сообщение об ошибке
```

### Дивіться також

-   [Throwable::getMessage()](throwable.getmessage.md) - Отримує повідомлення помилки
