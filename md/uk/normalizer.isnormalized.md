Перевірити, чи переданий рядок відповідає заданій формі нормалізації

-   [« Normalizer::getRawDecomposition](normalizer.getrawdecomposition.html)
    
-   [Normalizer::normalize »](normalizer.normalize.html)
    
-   [PHP Manual](index.html)
    
-   [Normalizer](class.normalizer.html)
    
-   Перевірити, чи переданий рядок відповідає заданій формі нормалізації
    

# Normalizer::isNormalized

# normalizerісnormalized

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Normalizer::isNormalized -- normalizerісnormalized — Перевірити, чи переданий рядок відповідає заданій формі нормалізації

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Normalizer::isNormalized(string $string, int $form = Normalizer::FORM_C): bool
```

Процедурний стиль

```methodsynopsis
normalizer_is_normalized(string $string, int $form = Normalizer::FORM_C): bool
```

Перевірити, чи переданий рядок відповідає заданій формі нормалізації.

### Список параметрів

`string`

Перевірений рядок

`form`

Одна із форм нормалізації.

### Значення, що повертаються

**`true`** якщо нормалізована та **`false`**, якщо ні або якщо сталася помилка

### Приклади

**Приклад #1 Приклад використання **normalizerісnormalized()****

```php
<?php
$char_A_ring = "\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)
$char_combining_ring_above = "\xCC\x8A";  // 'COMBINING RING ABOVE' (U+030A)

$char_orig = 'A' . $char_combining_ring_above;
$char_norm = normalizer_normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );

echo ( normalizer_is_normalized($char_orig, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
echo '; ';
echo ( normalizer_is_normalized($char_norm, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
?>
```

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

```php
<?php
$char_A_ring = "\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)
$char_combining_ring_above = "\xCC\x8A";  // 'COMBINING RING ABOVE' (U+030A)

$char_orig = 'A' . $char_combining_ring_above;
$char_norm = Normalizer::normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );

echo ( Normalizer::isNormalized($char_orig, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
echo '; ';
echo ( Normalizer::isNormalized($char_norm, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
?>
```

Результат виконання цього прикладу:

```
not normalized; normalized
```

### Дивіться також

-   [normalizer\_normalize()](normalizer.normalize.html) - Нормалізація рядка