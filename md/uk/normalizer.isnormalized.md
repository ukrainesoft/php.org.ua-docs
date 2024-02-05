---
navigation:
  - normalizer.getrawdecomposition.md: '« Normalizer::getRawDecomposition'
  - normalizer.normalize.md: 'Normalizer::normalize »'
  - index.md: PHP Manual
  - class.normalizer.md: Normalizer
title: 'Normalizer::isNormalized'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Normalizer::isNormalized

# normalizer\_is\_normalized

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Normalizer::isNormalized -- normalizer\_is\_normalized — Перевірити, чи переданий рядок відповідає заданій формі нормалізації

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

**Пример #1 Пример использования**normalizer\_is\_normalized()\*\*\*\*

```php
<?php
$char_A_ring = "\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)
$char_combining_ring_above = "\xCC\x8A";  // 'COMBINING RING ABOVE' (U+030A)

$char_orig = 'A' . $char_combining_ring_above;
$char_norm = normalizer_normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );

echo ( normalizer_is_normalized($char_orig, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
echo '; ';
echo ( normalizer_is_normalized($char_norm, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
?>
```

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

```php
<?php
$char_A_ring = "\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)
$char_combining_ring_above = "\xCC\x8A";  // 'COMBINING RING ABOVE' (U+030A)

$char_orig = 'A' . $char_combining_ring_above;
$char_norm = Normalizer::normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );

echo ( Normalizer::isNormalized($char_orig, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
echo '; ';
echo ( Normalizer::isNormalized($char_norm, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
?>
```

Результат виконання наведеного прикладу:

```
not normalized; normalized
```

### Дивіться також

-   [normalizer\_normalize()](normalizer.normalize.md) \- Нормалізація рядка
