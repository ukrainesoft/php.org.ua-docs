---
navigation:
  - function.recode-file.md: « recode\_file
  - function.recode.md: recode »
  - index.md: PHP Manual
  - ref.recode.md: Функції Recode
title: recode\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# recode\_string

(PHP 4, PHP 5, PHP 7 < 7.4.0)

recode\_string — Перекодує рядок відповідно до заданих параметрів

### Опис

```methodsynopsis
recode_string(string $request, string $string): string
```

Перекодирует строку`string` відповідно до `request`

### Список параметрів

`request`

Вибраний тип запиту на перекодування

`string`

Рядок для перекодування

### Значення, що повертаються

Повертає перекодований рядок (string) або **`false`**, якщо виникли проблеми з перекодуванням.

### Приклади

**Приклад #1 Приклад використання** recode\_string()\*\*\*\*

```php
<?php
echo recode_string("us..flat", "The following character has a diacritical mark: á");
?>
```

### Примітки

Простий запит на перекодування може бути "lat1..iso646-de".

### Дивіться також

-   Докладніше про запити на перекодування читайте у документації, яка входить до дистрибутиву GNU Recode.
-   [mb\_convert\_encoding()](function.mb-convert-encoding.md) \- Перетворює рядок з одного кодування символів на інший
-   [UConverter::transcode()](uconverter.transcode.md) \- Перетворює рядок з одного кодування символів на інший
-   [iconv()](function.iconv.md) \- Перетворює рядок з одного кодування символів на інший
