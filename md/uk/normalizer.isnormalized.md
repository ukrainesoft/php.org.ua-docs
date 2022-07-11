- [« Normalizer::getRawDecomposition](normalizer.getrawdecomposition.md)
- [Normalizer::normalize »](normalizer.normalize.md)

- [PHP Manual](index.md)
- [Normalizer](class.normalizer.md)
- Перевірити, чи відповідає переданий рядок заданій формі
нормалізації

# Normalizer::isNormalized

# normalizer_is_normalized

(PHP 5 = 5.3.0, PHP 7, PHP 8, PECL intl = 1.0.0)

Normalizer::isNormalized -- normalizer_is_normalized — Перевірити,
чи відповідає переданий рядок заданій формі нормалізації

### Опис

Об'єктно-орієнтований стиль

public static **Normalizer::isNormalized**(string `$string`, int `$form`
= Normalizer::FORM_C): bool

Процедурний стиль

**normalizer_is_normalized**(string `$string`, int `$form` =
Normalizer::FORM_C): bool

Перевірити, чи переданий рядок відповідає заданій формі
нормалізації.

### Список параметрів

`string`
Перевірений рядок

`form`
Одна із форм нормалізації.

### Значення, що повертаються

**`true`** якщо нормалізована та **`false`**, якщо ні або якщо відбулася
помилка

### Приклади

**Приклад #1 Приклад використання **normalizer_is_normalized()****

`<?php$char_A_ring=="\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)$char_combining_ring_above = "\xCC\x8A"; // 'COMBINING RING ABOVE' (U+030A)$char_orig = 'A' . $char_combining_ring_above;$char_norm = normalizer_normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );echo ( normalizer_is_normalized($char_orig, : ) "normalized" : "not normalized";echo '; ';echo ( normalizer_is_normalized($char_norm, Normalizer::FORM_C) ) ? "normalized" : "not normalized";?> `

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

`<?php$char_A_ring=="\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)$char_combining_ring_above = "\xCC\x8A"; // 'COMBINING RING ABOVE' (U+030A)$char_orig = 'A' . $char_combining_ring_above;$char_norm = Normalizer::normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );echo ( Normalizer::isNormalized( char "normalized" : "not normalized";echo '; ';echo ( Normalizer::isNormalized($char_norm, Normalizer::FORM_C) ) ? "normalized" : "not normalized";?> `

Результат виконання цього прикладу:

не normalized; normalized

### Дивіться також

- [normalizer_normalize()](normalizer.normalize.md) - Нормалізація
рядки
