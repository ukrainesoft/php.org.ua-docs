Кодує символ у числове HTML-посилання

-   [« mbencodemimeheader](function.mb-encode-mimeheader.html)
    
-   [мбencodingaliases »](function.mb-encoding-aliases.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з багатобайтовими рядками](ref.mbstring.html)
    
-   Кодує символ у числове HTML-посилання
    

# мбencodenumericentity

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбencodenumericentity — Кодує символ у числове HTML-посилання

### Опис

```methodsynopsis
mb_encode_numericentity(    string $string,    array $map,    ?string $encoding = null,    bool $hex = false): string
```

Перетворює задані коди символів у рядку (string) `string` з кодів у числові HTML-посилання.

### Список параметрів

`string`

Кодований рядок (string).

`map`

`map` - Масив, що задає діапазон кодів.

`encoding`

Параметр `encoding` є символьним кодуванням. Якщо він опущений або дорівнює **`null`**, замість нього буде використано значення внутрішнього кодування.

`hex`

Чи повинна сутність, що повертається, бути представлена ​​в шістнадцятковій нотації (інакше в десятковій)

### Значення, що повертаються

Сконвертований рядок (string).

### список змін

| Версия | Описание                                                    |
|--------|-------------------------------------------------------------|
|        | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання `map`**

```php
<?php
$convmap = array (
 int start_code1, int end_code1, int offset1, int mask1,
 int start_code2, int end_code2, int offset2, int mask2,
 ........
 int start_codeN, int end_codeN, int offsetN, int maskN );
// Задайте значения Юникода для start_codeN и end_codeN
// Добавьте к значению offsetN и сложите побитово с maskN,
// затем преобразуйте результат в число.
?>
```

**Приклад #2 Приклад використання **мбencodenumericentity()****

```php
<?php
/* Преобразование левой части ISO-8859-1 в числовую HTML-ссылку */
$convmap = array(0x80, 0xff, 0, 0xff);
$str = mb_encode_numericentity($str, $convmap, "ISO-8859-1");

/* Преобразование заданного пользователем SJIS-win кода в блоке в числовую ссыку*/
$convmap = array(
       0xe000, 0xe03e, 0x1040, 0xffff,
       0xe03f, 0xe0bb, 0x1041, 0xffff,
       0xe0bc, 0xe0fa, 0x1084, 0xffff,
       0xe0fb, 0xe177, 0x1085, 0xffff,
       0xe178, 0xe1b6, 0x10c8, 0xffff,
       0xe1b7, 0xe233, 0x10c9, 0xffff,
       0xe234, 0xe272, 0x110c, 0xffff,
       0xe273, 0xe2ef, 0x110d, 0xffff,
       0xe2f0, 0xe32e, 0x1150, 0xffff,
       0xe32f, 0xe3ab, 0x1151, 0xffff );
$str = mb_encode_numericentity($str, $convmap, "sjis-win");
?>
```

### Дивіться також

-   [мбdecodenumericentity()](function.mb-decode-numericentity.html) - Декодує посилання на числовий рядок HTML на символ