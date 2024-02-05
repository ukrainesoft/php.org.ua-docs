---
navigation:
  - exception.gettraceasstring.md: '« Exception::getTraceAsString'
  - exception.clone.md: 'Exception::\_\_clone »'
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Exception::\_\_function toString() { \[native code\] }

(PHP 5, PHP 7, PHP 8)

Exception::\_\_toString — Строкове подання винятку

### Опис

```methodsynopsis
public Exception::__toString(): string
```

Повертає виняток у вигляді рядка (string).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає виняток у вигляді рядка (string).

### Приклади

**Пример #1 Пример использования**Exception::\_\_toString()\*\*\*\*

```php
<?php
try {
    throw new Exception("Какое-нибудь сообщение об ошибке");
} catch(Exception $e) {
    echo $e;
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
exception 'Exception' with message 'Какое-нибудь сообщение об ошибке' in /home/bjori/tmp/ex.php:3
Stack trace:
#0 {main}
```

### Дивіться також

-   [Throwable::\_\_toString()](throwable.tostring.md) \- отримує рядкове подання викинутого об'єкта
