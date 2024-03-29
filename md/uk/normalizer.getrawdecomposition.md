---
navigation:
  - class.normalizer.md: « Normalizer
  - normalizer.isnormalized.md: 'Normalizer::isNormalized »'
  - index.md: PHP Manual
  - class.normalizer.md: Normalizer
title: 'Normalizer::getRawDecomposition'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Normalizer::getRawDecomposition

# normalizer\_get\_raw\_decomposition

(PHP 7 >= 7.3, PHP 8)

Normalizer::getRawDecomposition -- normalizer\_get\_raw\_decomposition — Витягує властивість Decomposition\_Mapping для заданого символу UTF-8

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Normalizer::getRawDecomposition(string $string, int $form = Normalizer::FORM_C): ?string
```

Процедурний стиль

```methodsynopsis
normalizer_get_raw_decomposition(string $string, int $form = Normalizer::FORM_C): ?string
```

Витягує властивість Decomposition\_Mapping, як визначено Unicode Character Database (UCD), для заданого символу UTF-8.

### Список параметрів

`string`

Рядок, який повинен являти собою одиничний символ у кодуванні UTF-8.

### Значення, що повертаються

Повертає рядок (string), що містить властивість Decomposition\_Mapping, якщо воно є у UCD.

Повертає **`null`** якщо для символу відсутня властивість Decomposition\_Mapping.

### Приклади

**Приклад #1 Приклад використання** Normalizer::getRawDecomposition()\*\*\*\*

```php
<?php

$result = "";
$strings = [
    "a",
    "\u{FFDA}",
    "\u{FDFA}",
    "",
    "aa",
    "\xF5",
];

foreach ($strings as $string) {
    $decomposition = Normalizer::getRawDecomposition($string);
    // $decomposition = normalizer_get_raw_decomposition($string); Процедурный стиль

    $error_code = intl_get_error_code();
    $error_message = intl_get_error_message();

    $string_hex = bin2hex($string);
    $result .= "---------------------\n";

    if ($decomposition === null) {
        $result .= "'$string_hex' не имеет соответствия декомпозиции\n" ;
    } else {
        $result .= "'$string_hex' имеет соответствие декомпозиции '" . bin2hex($decomposition) . "'\n" ;
    }

    $result .= "error info: '$error_message' ($error_code)\n";
}

echo $result;
?>
```

Результат виконання наведеного прикладу:

```
---------------------
'61' не имеет соответствия декомпозиции
error info: 'U_ZERO_ERROR' (0)
---------------------
'efbf9a' имеет соответствие декомпозиции 'e385a1'
error info: 'U_ZERO_ERROR' (0)
---------------------
'efb7ba' имеет соответствие декомпозиции 'd8b5d984d98920d8a7d984d984d98720d8b9d984d98ad98720d988d8b3d984d985'
error info: 'U_ZERO_ERROR' (0)
---------------------
'' не имеет соответствия декомпозиции
error info: 'Input string must be exactly one UTF-8 encoded code point long.: U_ILLEGAL_ARGUMENT_ERROR' (1)
---------------------
'6161' не имеет соответствия декомпозиции
error info: 'Input string must be exactly one UTF-8 encoded code point long.: U_ILLEGAL_ARGUMENT_ERROR' (1)
---------------------
'f5' не имеет соответствия декомпозиции
error info: 'Code point out of range: U_ILLEGAL_ARGUMENT_ERROR' (1)
```

### Дивіться також

-   [Normalizer::normalize()](normalizer.normalize.md) \- Нормалізація рядка
-   [Normalizer::isNormalized()](normalizer.isnormalized.md) \- Перевірити, чи переданий рядок відповідає заданій формі нормалізації
