---
navigation:
  - function.ucfirst.md: « ucfirst
  - function.utf8-decode.md: utf8decode »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: ucwords
---
# ucwords

(PHP 4, PHP 5, PHP 7, PHP 8)

ucwords — Перетворює на верхній регістр перший символ кожного слова в рядку

### Опис

```methodsynopsis
ucwords(string $string, string $separators = " \t\r\n\f\v"): string
```

Повертає рядок `string`, в якій перший символ кожного слова переведений у верхній регістр, якщо символ є буквою.

Для цієї функції слово - це рядок символів, які не перераховані в `separators`. За промовчанням це: пробіл, горизонтальна табуляція, повернення каретки, переклад рядка, розрив сторінки та вертикальна табуляція.

### Список параметрів

`string`

Вхідний рядок.

`separators`

Необов'язковий параметр `separators` містить символи розподільників слів.

### Значення, що повертаються

Повертає модифікований рядок.

### Приклади

**Приклад #1 Приклад використання **ucwords()****

```php
<?php
$foo = 'hello world!';
$foo = ucwords($foo);             // Hello World!

$bar = 'HELLO WORLD!';
$bar = ucwords($bar);             // HELLO WORLD!
$bar = ucwords(strtolower($bar)); // Hello World!
?>
```

**Приклад #2 Приклад **ucwords()** із заданим роздільником**

```php
<?php
$foo = 'hello|world!';
$bar = ucwords($foo);             // Hello|world!

$baz = ucwords($foo, "|");        // Hello|World!
?>
```

**Приклад #3 Приклад використання **ucwords()** з додатковими роздільниками**

```php
<?php
$foo = "mike o'hara";
$bar = ucwords($foo);                 // Mike O'hara

$baz = ucwords($foo, " \t\r\n\f\v'"); // Mike O'Hara
?>
```

### Примітки

> **Зауваження**: Функція залежить від локалі та оброблятиме введення відповідно до поточного встановленого мовного стандарту. Однак вона працює лише з однобайтовими наборами символів. Якщо вам потрібно використовувати багатобайтові символи (більшість мов, які не входять до Західної Європи), зверніть увагу на модулі [multibyte](book.mbstring.md) або [intl](book.intl.md) замість неї.

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [strtoupper()](function.strtoupper.md) - Перетворює рядок у верхній регістр
-   [strtolower()](function.strtolower.md) - Перетворює рядок на нижній регістр
-   [ucfirst()](function.ucfirst.md) - Перетворює перший символ рядка у верхній регістр
-   [мбconvertcase()](function.mb-convert-case.md) - Здійснює зміну регістру символів у рядку
