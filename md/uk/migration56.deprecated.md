---
navigation:
  - migration56.new-features.md: '" Нові можливості'
  - migration56.changed-functions.md: Змінені функції »
  - index.md: PHP Manual
  - migration56.md: Миграция с PHP 5.5.x на PHP 5.6.x
title: 'Функціонал, оголошений застарілим у PHP 5.6.x'
---
## Функціонал, оголошений застарілим у PHP 5.6.x

### Дзвінки з несумісного контексту

Методи, що викликаються з несумісного контексту, оголошені застарілими і викликатимуть помилку рівня **`E_DEPRECATED`** замість **`E_STRICT`**. У майбутніх версіях PHP підтримка цих дзвінків буде видалена.

Приклад такого виклику є:

```php
<?php
class A {
    function f() { echo get_class($this); }
}

class B {
    function f() { A::f(); }
}

(new B)->f();
?>
```

Результат виконання цього прикладу:

```
Deprecated: Non-static method A::f() should not be called statically, assuming $this from incompatible context in - on line 7
B
```

### $HTTPRAWPOSTDATA та `always_populate_raw_post_data`

`always_populate_raw_post_data` тепер буде викликати помилку \*\*`E_DEPRECATED`\*\*якщо $HTTPRAWPOSTDATA заповнено. Новий код має використовувати [`php://input`](wrappers.php.md#wrappers.php.input) замість $HTTPRAWPOSTDATA, який буде видалено у майбутніх версіях PHP. Ви можете вибрати нову поведінку (у якій $HTTPRAWPOSTDATA ніколи не визначається, отже, **`E_DEPRECATED`** не буде генерувати помилку) шляхом установки `always_populate_raw_post_data` в `-1`

### Налаштування кодування [iconv](book.iconv.md) і [mbstring](book.mbstring.md)

Параметри конфігурації [iconv](book.iconv.md) і [mbstring](book.mbstring.md), пов'язані з кодуванням, застаріли на користь [`default_charset`](ini.core.md#ini.default-charset). Застарілі опції:

-   [`iconv.input_encoding`](iconv.configuration.md#ini.iconv.input-encoding)
-   [`iconv.output_encoding`](iconv.configuration.md#ini.iconv.output-encoding)
-   [`iconv.internal_encoding`](iconv.configuration.md#ini.iconv.internal-encoding)
-   [`mbstring.http_input`](mbstring.configuration.md#ini.mbstring.http-input)
-   [`mbstring.http_output`](mbstring.configuration.md#ini.mbstring.http-output)
-   [`mbstring.internal_encoding`](mbstring.configuration.md#ini.mbstring.internal-encoding)
