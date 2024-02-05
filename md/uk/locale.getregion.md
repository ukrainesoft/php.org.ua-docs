---
navigation:
  - locale.getprimarylanguage.md: '« Locale::getPrimaryLanguage'
  - locale.getscript.md: 'Locale::getScript »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getRegion'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::getRegion

# locale\_get\_region

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getRegion -- locale\_get\_region — Отримати регіон для локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getRegion(string $locale): ?string
```

Процедурний стиль

```methodsynopsis
locale_get_region(string $locale): ?string
```

Отримує регіон для локалі.

### Список параметрів

`locale`

Локаль для отримання коду регіону

### Значення, що повертаються

Код регіону, пов'язаний з локаллю або \*\*`null`\*\*якщо відсутня.

Повертає \*\*`null`\*\*якщо довжина `locale` перевищує **`INTL_MAX_LOCALE_LEN`**

### Приклади

**Приклад #1 Приклад використання** locale\_get\_region()\*\*\*\*

```php
<?php
echo locale_get_region('de-CH-1901');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getRegion('de-CH-1901');
?>
```

Результат виконання наведеного прикладу:

```
CH
```

### Дивіться також

-   [locale\_get\_primary\_language()](locale.getprimarylanguage.md) \- Отримати первинну мову для локалі
-   [locale\_get\_script()](locale.getscript.md) \- Отримати алфавіт для локалі
-   [locale\_get\_all\_variants()](locale.getallvariants.md) \- Отримання варіантів із переданої локалі
