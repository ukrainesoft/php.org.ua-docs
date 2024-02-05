---
navigation:
  - locale.getregion.md: '« Locale::getRegion'
  - locale.lookup.md: 'Locale::lookup »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getScript'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::getScript

# locale\_get\_script

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getScript -- locale\_get\_script — Отримати алфавіт для локалі

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

**Приклад #1 Приклад використання** locale\_get\_script()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
Cyrl
```

### Дивіться також

-   [locale\_get\_primary\_language()](locale.getprimarylanguage.md) \- Отримати первинну мову для локалі
-   [locale\_get\_region()](locale.getregion.md) \- Отримати регіон для локалі
-   [locale\_get\_all\_variants()](locale.getallvariants.md) \- Отримання варіантів із переданої локалі
