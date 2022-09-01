---
navigation:
  - locale.getkeywords.html: '« Locale::getKeywords'
  - locale.getregion.html: 'Locale::getRegion »'
  - index.html: PHP Manual
  - class.locale.html: Locale
title: 'Locale::getPrimaryLanguage'
---
# Locale::getPrimaryLanguage

# localegetprimarylanguage

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getPrimaryLanguage -- localegetprimarylanguage — Отримати первинну мову для локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getPrimaryLanguage(string $locale): ?string
```

Процедурний стиль

```methodsynopsis
locale_get_primary_language(string $locale): ?string
```

Отримує первинну мову для локалі.

### Список параметрів

`locale`

Локаль для отримання первинної мови

### Значення, що повертаються

Код мови, пов'язаний із локаллю.

Повертає \*\*`null`\*\*якщо довжина `locale` перевищує **`INTL_MAX_LOCALE_LEN`**

### Приклади

**Приклад #1 Приклад використання **localegetprimarylanguage()****

```php
<?php
echo locale_get_primary_language('zh-Hant');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getPrimaryLanguage('zh-Hant');
?>
```

Результат виконання цього прикладу:

```
zh
```

### Дивіться також

-   [localegetscript()](locale.getscript.html) - Отримати алфавіт для локалі
-   [localegetregion()](locale.getregion.html) - Отримати регіон для локалі
-   [localegetallvariants()](locale.getallvariants.html) - Отримання варіантів із переданої локалі
