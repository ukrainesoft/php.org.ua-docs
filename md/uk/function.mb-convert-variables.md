Перетворює символи на змінну з одного кодування на інше

-   [« mbconvertkana](function.mb-convert-kana.html)
    
-   [мбdecodemimeheader »](function.mb-decode-mimeheader.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з багатобайтовими рядками](ref.mbstring.html)
    
-   Перетворює символи на змінну з одного кодування на інше
    

# мбconvertvariables

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбconvertvariables — Перетворює символи на змінну з одного кодування на інше

### Опис

```methodsynopsis
mb_convert_variables(    string $to_encoding,    array|string $from_encoding,    mixed &$var,    mixed &...$vars): string|false
```

Конвертує символи в змінних `var` і `vars` з кодування `from_encoding` у кодування `to_encoding`

**мбconvertvariables()** об'єднує рядки з масиву чи об'єкта визначення їх кодування, оскільки у разі коротких рядків визначити кодування часто не вдається. Внаслідок цього неприпустимо поміщати в один масив або об'єкт рядка в різних кодуваннях.

### Список параметрів

`to_encoding`

Кодування, в яке потрібно перекодувати рядок (string).

`from_encoding`

`from_encoding` задається у вигляді масиву (array) або рядка (string) з розділеними комами кодуванням. Функція спробує визначити кодування вихідного рядка на основі списку можливих кодувань в аргументі `from-coding`. Якщо `from_encoding` опущений, використовується `detect_order`

`var`

`var` - Посилання на змінну, вміст якої необхідно перетворити. Це може бути рядок, масив чи об'єкт . **мбconvertvariables()** приймає, що це аргументи мають однакову кодування.

`vars`

Додаткові `var`

### Значення, що повертаються

Вихідне кодування у разі успішного виконання або **`false`** у разі невдачі.

### Приклади

**Приклад #1 Приклад використання **мбconvertvariables()****

```php
<?php
/* Преобразование переменных $post1, $post2 во внутреннюю кодировку скрипта */
$interenc = mb_internal_encoding();
$inputenc = mb_convert_variables($interenc, "ASCII,UTF-8,SJIS-win", $post1, $post2);
?>
```