---
navigation:
  - function.register-shutdown-function.md: « register\_shutdown\_function
  - function.unregister-tick-function.md: unregister\_tick\_function »
  - index.md: PHP Manual
  - ref.funchand.md: Функції керування функціями
title: register\_tick\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# register\_tick\_function

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

register\_tick\_function — Реєструє функцію для виконання при кожному тику

### Опис

```methodsynopsis
register_tick_function(callable $callback, mixed ...$args): bool
```

Реєструє функцію `callback`, яка повинна викликатись при кожному [тиці](control-structures.declare.md#control-structures.declare.ticks)

### Список параметрів

`callback`

Реєстрована функція.

`args`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** register\_tick\_function()\*\*\*\*

```php
<?php
declare(ticks=1);

// использование функции в качестве обратного вызова
register_tick_function('my_function', true);

// использование метода объекта
$object = new my_class();
register_tick_function(array($object, 'my_method'), true);
?>
```

### Дивіться також

-   [declare](control-structures.declare.md)
-   [unregister\_tick\_function()](function.unregister-tick-function.md) \- Видаляє функцію зі списку зареєстрованих для виконання на кожному тику
