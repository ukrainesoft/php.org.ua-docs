---
navigation:
  - locale.getkeywords.md: '« Locale::getKeywords'
  - locale.getregion.md: 'Locale::getRegion »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getPrimaryLanguage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::getPrimaryLanguage

# locale\_get\_primary\_language

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getPrimaryLanguage -- locale\_get\_primary\_language — Отримати первинну мову для локалі

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

**Пример #1 Пример использования**locale\_get\_primary\_language()\*\*\*\*

```php
<?php
echo locale_get_primary_language('zh-Hant');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getPrimaryLanguage('zh-Hant');
?>
```

Результат виконання наведеного прикладу:

```
zh
```

### Дивіться також

-   [locale\_get\_script()](locale.getscript.md) \- Отримати алфавіт для локалі
-   [locale\_get\_region()](locale.getregion.md) \- Отримати регіон для локалі
-   [locale\_get\_all\_variants()](locale.getallvariants.md) \- Отримання варіантів із переданої локалі
