---
navigation:
  - function.ucfirst.md: « ucfirst
  - function.utf8-decode.md: utf8\_decode »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: ucwords
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ucwords

(PHP 4, PHP 5, PHP 7, PHP 8)

ucwords — Перетворює у верхній регістр перший символ кожного слова у рядку

### Опис

```methodsynopsis
ucwords(string $string, string $separators = " \t\r\n\f\v"): string
```

Повертає рядок `string`, в якій перший символ кожного слова переведений у верхній регістр, якщо цей символ є символом ASCII між `"a"`(0x61) и`"z"`(0x7a).

Для цієї функції слово - це рядок символів, які не перераховані в `separators`. За промовчанням це: пробіл, горизонтальна табуляція, повернення каретки, переклад рядка, розрив сторінки та вертикальна табуляція.

Щоб зробити аналогічне перетворення багатобайтових рядків, скористайтеся функцією [mb\_convert\_case()](function.mb-convert-case.md) з режимом **`MB_CASE_TITLE`**

### Список параметрів

`string`

Вхідний рядок.

`separators`

Необов'язковий параметр `separators` містить символи розподільників слів.

### Значення, що повертаються

Повертає модифікований рядок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Перетворення регістру більше не залежить від локалі, встановленої за допомогою функції [setlocale()](function.setlocale.md). . Буде перетворено лише символи ASCII. |

### Приклади

**Пример #1 Пример использования**ucwords()\*\*\*\*

```php
<?php
$foo = 'hello world!';
$foo = ucwords($foo);             // Hello World!

$bar = 'HELLO WORLD!';
$bar = ucwords($bar);             // HELLO WORLD!
$bar = ucwords(strtolower($bar)); // Hello World!
?>
```

**Пример #2 Пример**ucwords()\*\* із заданим роздільником\*\*

```php
<?php
$foo = 'hello|world!';
$bar = ucwords($foo);             // Hello|world!

$baz = ucwords($foo, "|");        // Hello|World!
?>
```

**Пример #3 Пример использования**ucwords()\*\* з додатковими роздільниками\*\*

```php
<?php
$foo = "mike o'hara";
$bar = ucwords($foo);                 // Mike O'hara

$baz = ucwords($foo, " \t\r\n\f\v'"); // Mike O'Hara
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [strtoupper()](function.strtoupper.md) \- Перетворює рядок у верхній регістр
-   [strtolower()](function.strtolower.md) \- Перетворює рядок на нижній регістр
-   [ucfirst()](function.ucfirst.md) \- Перетворює перший символ рядка у верхній регістр
-   [mb\_convert\_case()](function.mb-convert-case.md) \- Змінює регістр символів у рядку
