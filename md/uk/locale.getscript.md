---
navigation:
  - locale.getregion.md: '« Locale::getRegion'
  - locale.lookup.md: 'Locale::lookup »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getScript'
---
# Locale::getScript

# localegetscript

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getScript -- localegetscript — Отримати алфавіт для локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getScript(string $locale): ?string
```

Процедурний стиль

```methodsynopsis
locale_get_script(string $locale): ?string
```

Отримує абетку для локалі.

### Список параметрів

`locale`

Локаль для отримання алфавіту

### Значення, що повертаються

Алфавіт, пов'язаний з локаллю або \*\*`null`\*\*якщо відсутня.

### Приклади

**Приклад #1 Приклад використання **localegetscript()****

```php
<?php
echo locale_get_script('sr-Cyrl');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getScript('sr-Cyrl');
?>
```

Результат виконання цього прикладу:

```
Cyrl
```

### Дивіться також

-   [localegetprimarylanguage()](locale.getprimarylanguage.md) - Отримати первинну мову для локалі
-   [localegetregion()](locale.getregion.md) - Отримати регіон для локалі
-   [localegetallvariants()](locale.getallvariants.md) - Отримання варіантів із переданої локалі
