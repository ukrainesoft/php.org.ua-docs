---
navigation:
  - exception.gettrace.md: '« Exception::getTrace'
  - exception.tostring.md: 'Exception::\_\_toString »'
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::getTraceAsString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Exception::getTraceAsString

(PHP 5, PHP 7, PHP 8)

Exception::getTraceAsString — Отримує трасування стека у вигляді рядка

### Опис

```methodsynopsis
final public Exception::getTraceAsString(): string
```

Повертає трасування стека виключення у вигляді рядка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає трасування стека виключення у вигляді рядка.

### Приклади

**Пример #1 Пример использования**Exception::getTraceAsString()\*\*\*\*

```php
<?php
function test() {
    throw new Exception;
}

try {
    test();
} catch(Exception $e) {
    echo $e->getTraceAsString();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
#0 /home/bjori/tmp/ex.php(7): test()
#1 {main}
```

### Дивіться також

-   [Throwable::getTraceAsString()](throwable.gettraceasstring.md) \- Отримує результати трасування стека у вигляді рядка
