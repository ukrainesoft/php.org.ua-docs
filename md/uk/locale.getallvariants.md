---
navigation:
  - locale.filtermatches.md: '« Locale::filterMatches'
  - locale.getdefault.md: 'Locale::getDefault »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getAllVariants'
---
# Locale::getAllVariants

# localegetallvariants

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getAllVariants -- localegetallvariants — Отримання варіантів із переданої локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getAllVariants(string $locale): ?array
```

Процедурний стиль

```methodsynopsis
locale_get_all_variants(string $locale): ?array
```

Отримання варіантів із переданої локалі

### Список параметрів

`locale`

Локаль з якої буде вилучено варіанти

### Значення, що повертаються

Масив, що містить список варіантів заданої локалі, або **`null`**, якщо таких немає

Повертає \*\*`null`\*\*якщо довжина `locale` перевищує **`INTL_MAX_LOCALE_LEN`**

### Приклади

**Приклад #1 Приклад використання **localegetallvariants()****

```php
<?php
$arr = locale_get_all_variants('sl_IT_NEDIS_ROJAZ_1901');
var_export( $arr );
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
 $arr = Locale::getAllVariants('sl_IT_NEDIS_ROJAZ_1901');
 var_export( $arr );
?>
```

Результат виконання цього прикладу:

```
array (
    0 => 'NEDIS',
    1 => 'ROJAZ',
    2 => '1901',
)
```

### Дивіться також

-   [localegetprimarylanguage()](locale.getprimarylanguage.md) - Отримати первинну мову для локалі
-   [localegetscript()](locale.getscript.md) - Отримати алфавіт для локалі
-   [localegetregion()](locale.getregion.md) - Отримати регіон для локалі
