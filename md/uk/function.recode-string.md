Перекодує рядок відповідно до заданих параметрів

-   [« recodefile](function.recode-file.html)
    
-   [recode »](function.recode.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Recode](ref.recode.html)
    
-   Перекодує рядок відповідно до заданих параметрів
    

# recodestring

(PHP 4, PHP 5, PHP 7 < 7.4.0)

recodestring — Перекодує рядок відповідно до заданих параметрів

### Опис

```methodsynopsis
recode_string(string $request, string $string): string
```

Перекодує рядок `string` відповідно до `request`

### Список параметрів

`request`

Вибраний тип запиту на перекодування

`string`

Рядок для перекодування

### Значення, що повертаються

Повертає перекодований рядок (string) або **`false`**, якщо виникли проблеми з перекодуванням.

### Приклади

**Приклад #1 Приклад використання **recodestring()****

```php
<?php
echo recode_string("us..flat", "The following character has a diacritical mark: á");
?>
```

### Примітки

Простий запит на перекодування може бути "lat1..iso646-de".

### Дивіться також

-   Докладніше про запити на перекодування читайте у документації, яка входить до дистрибутиву GNU Recode.
-   [мбconvertencoding()](function.mb-convert-encoding.html) - Перетворює рядок з одного кодування символів на інший
-   [UConverter::transcode()](uconverter.transcode.html) - Перетворює рядок з одного кодування символів на інший
-   [iconv()](function.iconv.html) - Перетворює рядок з одного кодування символів на інший