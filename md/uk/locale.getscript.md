Отримати алфавіт для локалі

-   [« Locale::getRegion](locale.getregion.html)
    
-   [Locale::lookup »](locale.lookup.html)
    
-   [PHP Manual](index.html)
    
-   [Locale](class.locale.html)
    
-   Отримати алфавіт для локалі
    

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

Алфавіт, пов'язаний з локаллю або **`null`**якщо відсутня.

### Приклади

**Приклад #1 Приклад використання **localegetscript()****

```php
<?php
echo locale_get_script('sr-Cyrl');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getScript('sr-Cyrl');
?>
```

Результат виконання цього прикладу:

```
Cyrl
```

### Дивіться також

-   [locale\_get\_primary\_language()](locale.getprimarylanguage.html) - Отримати первинну мову для локалі
-   [locale\_get\_region()](locale.getregion.html) - Отримати регіон для локалі
-   [locale\_get\_all\_variants()](locale.getallvariants.html) - Отримання варіантів із переданої локалі