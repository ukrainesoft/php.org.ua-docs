---
navigation:
  - error.construct.md: '« Error::\_\_construct'
  - error.getprevious.md: 'Error::getPrevious »'
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::getMessage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Error::getMessage

(PHP 7, PHP 8)

Error::getMessage — Отримує повідомлення про помилку

### Опис

```methodsynopsis
final public Error::getMessage(): string
```

Повертає повідомлення про помилку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення про помилку у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання** Error::getMessage()\*\*\*\*

```php
<?php
try {
    throw new Error("Страшная ошибка");
} catch(Error $e) {
    echo $e->getMessage();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Страшная ошибка
```

### Дивіться також

-   [Throwable::getMessage()](throwable.getmessage.md) \- Отримує повідомлення помилки
