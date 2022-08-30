Повертає відповідним чином локалізовану назву регіону для заданої локалі

-   [« Locale::getDisplayName](locale.getdisplayname.html)
    
-   [Locale::getDisplayScript »](locale.getdisplayscript.html)
    
-   [PHP Manual](index.html)
    
-   [Locale](class.locale.html)
    
-   Повертає відповідним чином локалізовану назву регіону для заданої локалі
    

# Locale::getDisplayRegion

# localegetdisplayregion

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getDisplayRegion -- localegetdisplayregion — Повертає відповідним чином локалізовану назву регіону для заданої локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getDisplayRegion(string $locale, ?string $displayLocale = null): string|false
```

Процедурний стиль

```methodsynopsis
locale_get_display_region(string $locale, ?string $displayLocale = null): string|false
```

Повертає відповідним чином локалізовану назву регіону для заданої локалі. Якщо **`null`**, то буде використано локаль за замовчуванням.

### Список параметрів

`locale`

Локаль.

`displayLocale`

Необов'язковий локаль для форматування

### Значення, що повертаються

Назва регіону для `locale` у форматі локалі `displayLocale` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                      |
|--------|-----------------------------------------------|
|        | `displayLocale` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **localegetdisplayregion()****

```php
<?php
echo locale_get_display_region('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_region('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_region('sl-Latn-IT-nedis', 'de');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getDisplayRegion('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayRegion('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayRegion('sl-Latn-IT-nedis', 'de');
?>
```

Результат виконання цього прикладу:

```
Italy;
Italie;
Italien
```

### Дивіться також

-   [localegetdisplayname()](locale.getdisplayname.html) - Повертає відповідним чином локалізоване ім'я локалі
-   [localegetdisplaylanguage()](locale.getdisplaylanguage.html) - Повертає відповідним чином локалізоване ім'я мови для заданої локалі
-   [localegetdisplayscript()](locale.getdisplayscript.html) - Повертає відповідним чином локалізовану назву алфавіту для заданої локалі
-   [localegetdisplayvariant()](locale.getdisplayvariant.html) - Повертає відповідним чином локалізовану назву варіанта для заданої локалі