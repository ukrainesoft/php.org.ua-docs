---
navigation:
  - function.mb-decode-mimeheader.md: « mb\_decode\_mimeheader
  - function.mb-detect-encoding.md: mb\_detect\_encoding »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_decode\_numericentity
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_decode\_numericentity

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_decode\_numericentity — Декодує посилання на числовий рядок HTML символ

### Опис

```methodsynopsis
mb_decode_numericentity(string $string, array $map, ?string $encoding = null): string
```

Перетворює рядок чисел `string` (string) у заданому блоці символ.

### Список параметрів

`string`

Рядок (string) для декодування.

`map`

Параметр`map` - Масив (array), який задає область коду для перетворення.

`encoding`

Параметр`encoding` - Це кодування символів. Якщо він опущений або дорівнює **`null`**, для нього буде встановлено внутрішнє кодування символів.

`is_hex`

Параметр оголошено застарілим.

### Значення, що повертаються

Повертає перетворений рядок (string).

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад использования параметра`map`**

```php
<?php
$convmap = array (
   int start_code1, int end_code1, int offset1, int mask1,
   int start_code2, int end_code2, int offset2, int mask2,
   ........
   int start_codeN, int end_codeN, int offsetN, int maskN );
// Задайте значения Юникода для start_codeN и end_codeN
// Добавьте к значению offsetN и сложите побитово с maskN,
// затем преобразуйте результат в число.
?>
```

**Приклад #2 Приклад екранування рядка JavaScript через параметр `map`**

```php
<?php
function escape_javascript_string($str) {
  $map = [
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,0,0, // 49
          0,0,0,0,0,0,0,0,1,1,
          1,1,1,1,1,0,0,0,0,0,
          0,0,0,0,0,0,0,0,0,0,
          0,0,0,0,0,0,0,0,0,0,
          0,1,1,1,1,1,1,0,0,0, // 99
          0,0,0,0,0,0,0,0,0,0,
          0,0,0,0,0,0,0,0,0,0,
          0,0,0,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1, // 149
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1, // 199
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1, // 249
          1,1,1,1,1,1,1, // 255
          ];
  // Кодировка символа UTF-8
  $mblen = mb_strlen($str, 'UTF-8');
  $utf32 = bin2hex(mb_convert_encoding($str, 'UTF-32', 'UTF-8'));
  for ($i=0, $encoded=''; $i < $mblen; $i++) {
      $u = substr($utf32, $i*8, 8);
      $v = base_convert($u, 16, 10);
      if ($v < 256 && $map[$v]) {
        $encoded .= '\\x'.substr($u, 6,2);
      } else if ($v == 2028) {
        $encoded .= '\\u2028';
      } else if ($v == 2029) {
        $encoded .= '\\u2029';
      } else {
        $encoded .= mb_convert_encoding(hex2bin($u), 'UTF-8', 'UTF-32');
      }
   }
   return $encoded;
}

// Данные для теста
$convmap = [ 0x0, 0xffff, 0, 0xffff ];
$msg = '';
for ($i=0; $i < 1000; $i++) {
  // Функция chr() не может сгенерировать корректный символ UTF-8 больший, чем 128. Используем функцию mb_decode_numericentity().
  $msg .= mb_decode_numericentity('&#'.$i.';', $convmap, 'UTF-8');
}

// var_dump($msg);
var_dump(escape_javascript_string($msg));
```

### Дивіться також

-   [mb\_encode\_numericentity()](function.mb-encode-numericentity.md) \- Кодує символ у числове HTML-посилання
