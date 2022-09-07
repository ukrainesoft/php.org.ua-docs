---
navigation:
  - ffi.examples-basic.md: « Прості приклади використання FFI
  - ffi.examples-complete.md: Комплексний приклад PHP/FFI/preloading »
  - index.md: PHP Manual
  - ffi.examples.md: Приклади
title: Callback-функції PHP
---
## Callback-функції PHP

Можна привласнити замикання PHP змінної типу "покажчик" (pointer) або передати його як аргумент функції:

```php
<?php
$zend = FFI::cdef("
    typedef int (*zend_write_func_t)(const char *str, size_t str_length);
    extern zend_write_func_t zend_write;
");

echo "Привет, мир 1!\n";

$orig_zend_write = clone $zend->zend_write;
$zend->zend_write = function($str, $len) {
    global $orig_zend_write;
    $orig_zend_write("{\n\t", 3);
    $ret = $orig_zend_write($str, $len);
    $orig_zend_write("}\n", 2);
    return $ret;
};
echo "Привет, мир 2!\n";
$zend->zend_write = $orig_zend_write;
echo "Привет, мир 3!\n";
?>
```

Результат виконання цього прикладу:

```
Привет, мир 1!
{
        Привет, мир 2!
}
Привет, мир 3!
```

Хоча це і працює, але ця функціональність підтримується не на всіх платформах libffi, не є ефективною і викликає витік ресурсів при завершенні запитів.

**Підказка**

Тому рекомендується мінімізувати використання callback-функцій PHP.
