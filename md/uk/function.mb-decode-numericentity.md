- [« mb_decode_mimeheader](function.mb-decode-mimeheader.md)
- [mb_detect_encoding »](function.mb-detect-encoding.md)

- [PHP Manual](index.md)
- [Функції для роботи з багатобайтовими рядками](ref.mbstring.md)
- Декодує посилання на числовий рядок HTML на символ

#mb_decode_numericentity

(PHP 4 \>= 4.0.6, PHP 5, PHP 7, PHP 8)

mb_decode_numericentity — Декодує посилання на числовий рядок HTML
символ

### Опис

**mb_decode_numericentity**(string `$string`, array `$map`, ?string
`$encoding` = **`null`**): string

Перетворює рядок чисел `string` (string) у заданому блоці на символ.

### Список параметрів

`string`
Рядок (string) для декодування.

`map`
`map` - масив (array), який визначає діапазон кодів символів.

`encoding`
Параметр 'encoding' є символьним кодуванням. Якщо він
опущений або дорівнює **`null`**, замість нього буде використано значення
внутрішнього кодування.

`is_hex`
Параметр не використовується.

### Значення, що повертаються

Перетворений рядок (string).

### Список змін

| Версія | Опис                                                     |
|--------|----------------------------------------------------------|
| 8.0.0  | Тепер параметр encoding може набувати значення **null**. |

### Приклади

**Приклад #1 Приклад використання `map`**

` <?php$convmap = array (   int start_code1, int end_code1, int offset1, int mask1,   int start_code2, int end_code2, int offset2, int mask2,   ........   int start_codeN, int end_codeN, int offsetN, int maskN );// Задайте значення Юнікоду для start_codeN і end_codeN// Додайте до|значення offsetN і складіть побитово з|

**Приклад #2 Приклад екранування рядка JavaScript за допомогою `map`**

` <?phpfunction escape_javascript_string($str) {  $map = [          1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1 1,1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1,1,1,1,1,0,0, // 49 0,0,0,0,0,0,0,1,1, 1,1,1,1,1,0,0 ,0,0,0,          0,0,0,0,0,0,0,0,0,0                 ,1,1,1,1,1,0,0,0,//99          0,0,0,0,0,0,0,0,0,0,          0,0,0,0,0, 0,0,0,0,0,          0,0,0,1,1,1,1,1,1,1,         1,1,1,1,1,1,1,1,1,1,1, 1,1,1,1,1,1,1,1,1,1, 1/149 1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1 ,1,1,1,1,1,1,          1,1,1,1,1,1,1,1,1,1,         1,1,1,1,1,1,1,1,1,1 1,1,1,1,1,1,1,               1,1,1,1,1,1,1,1,          1,1,1,1,1,1,1,1,1,1,         1,1,1,1,1,1,1,1, 1,1,1, 1,1,1,1,1,1,1,1,1,1,1/1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1 //Кодування символу UTF-8 $mblen = mb_strlen($str, 'UTF-8'); $utf32 = bin2hex(mb_convert_encoding($str, 'UTF-32', 'UTF-8')); for ($i=0, $encoded=''; $i < $mblen; $i++) {     $u = substr($utf32, $i*8, 8); $v = base_convert($u, 16, 10); if ($v < 256 && $map[$v]) {        $encoded .= '\x'.substr($u, 6,2); } else if ($v == 2028) {        $encoded .= '\u2028'; } else if ($v == 2029) {        $encoded .= '\u2029'; } else {        $encoded .= mb_convert_encoding(hex2bin($u), 'UTF-8', 'UTF-32'); }  }}  return $encoded;}// Дані для тесту$convmap = [ 0x0, 0xffff, 0, 0xffff ];$msg = '';for ($i=0;          () не може згенерувати коректний символ UTF-8 більший, чем 128. Використовуємо mb_decode_numericentity(). $msg .= mb_decode_numericentity('&#'.$i.';', $convmap, 'UTF-8');}// var_dump($msg);var_dump(escape_javascript_string($msg)); `

### Дивіться також

- [mb_encode_numericentity()](function.mb-encode-numericentity.md) -
Кодує символ у числове HTML-посилання
