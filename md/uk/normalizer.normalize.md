Нормалізація рядка

-   [« Normalizer::isNormalized](normalizer.isnormalized.html)
    
-   [MessageFormatter »](class.messageformatter.html)
    
-   [PHP Manual](index.html)
    
-   [Normalizer](class.normalizer.html)
    
-   Нормалізація рядка
    

# Normalizer::normalize

# normalizernormalize

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Normalizer::normalize -- normalizernormalize - Нормалізація рядка

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Normalizer::normalize(string $string, int $form = Normalizer::FORM_C): string|false
```

Процедурний стиль

```methodsynopsis
normalizer_normalize(string $string, int $form = Normalizer::FORM_C): string|false
```

Нормалізує переданий рядок

### Список параметрів

`string`

Рядок для нормалізації

`form`

Одна з форм нормалізації

### Значення, що повертаються

Нормалізований рядок або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **normalizernormalize()****

```php
<?php
$char_A_ring = "\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)
$char_combining_ring_above = "\xCC\x8A";  // 'COMBINING RING ABOVE' (U+030A)

$char_1 = normalizer_normalize( $char_A_ring, Normalizer::FORM_C );
$char_2 = normalizer_normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );

echo urlencode($char_1);
echo ' ';
echo urlencode($char_2);
?>
```

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

```php
<?php
$char_A_ring = "\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)
$char_combining_ring_above = "\xCC\x8A";  // 'COMBINING RING ABOVE' (U+030A)

$char_1 = Normalizer::normalize( $char_A_ring, Normalizer::FORM_C );
$char_2 = Normalizer::normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );

echo urlencode($char_1);
echo ' ';
echo urlencode($char_2);
?>
```

Результат виконання цього прикладу:

```
%C3%85 %C3%85
```

### Дивіться також

-   [normalizer\_is\_normalized()](normalizer.isnormalized.html) - Перевірити, чи переданий рядок відповідає заданій формі нормалізації