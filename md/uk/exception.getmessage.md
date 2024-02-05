---
navigation:
  - exception.construct.md: '« Exception::\_\_construct'
  - exception.getprevious.md: 'Exception::getPrevious »'
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::getMessage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Пример #1 Пример использования**Exception::getMessage()\*\*\*\*

```php
<?php
try {
    throw new Exception("Какое-нибудь сообщение об ошибке");
} catch(Exception $e) {
    echo $e->getMessage();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Какое-нибудь сообщение об ошибке
```

### Дивіться також

-   [Throwable::getMessage()](throwable.getmessage.md) \- Отримує повідомлення помилки
