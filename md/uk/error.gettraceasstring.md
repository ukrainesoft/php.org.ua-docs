---
navigation:
  - error.gettrace.md: '« Error::getTrace'
  - error.tostring.md: 'Error::\_\_toString »'
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::getTraceAsString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Error::getTraceAsString

(PHP 7, PHP 8)

Error::getTraceAsString — Отримує трасування стека у вигляді рядка

### Опис

```methodsynopsis
final public Error::getTraceAsString(): string
```

Повертає трасування стека у вигляді рядка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає трасування стека у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання** Error::getTraceAsString()\*\*\*\*

```php
<?php
function test() {
    throw new Error;
}

try {
    test();
} catch(Error $e) {
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
