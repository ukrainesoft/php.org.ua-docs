---
navigation:
  - locale.getprimarylanguage.html: '« Locale::getPrimaryLanguage'
  - locale.getscript.html: 'Locale::getScript »'
  - index.html: PHP Manual
  - class.locale.html: Locale
title: 'Locale::getRegion'
---
# Locale::getRegion

# localegetregion

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getRegion -- localegetregion — Отримати регіон для локалі

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

**Приклад #1 Приклад використання **localegetregion()****

```php
<?php
echo locale_get_region('de-CH-1901');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getRegion('de-CH-1901');
?>
```

Результат виконання цього прикладу:

```
CH
```

### Дивіться також

-   [localegetprimarylanguage()](locale.getprimarylanguage.html) - Отримати первинну мову для локалі
-   [localegetscript()](locale.getscript.html) - Отримати алфавіт для локалі
-   [localegetallvariants()](locale.getallvariants.html) - Отримання варіантів із переданої локалі
