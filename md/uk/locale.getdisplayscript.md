Повертає відповідним чином локалізовану назву алфавіту для заданої локалі

-   [« Locale::getDisplayRegion](locale.getdisplayregion.md)
    
-   [Locale::getDisplayVariant »](locale.getdisplayvariant.md)
    
-   [PHP Manual](index.md)
    
-   [Locale](class.locale.md)
    
-   Повертає відповідним чином локалізовану назву алфавіту для заданої локалі
    

# Locale::getDisplayScript

# localegetdisplayscript

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getDisplayScript -- localegetdisplayscript — Повертає відповідним чином локалізовану назву алфавіту для заданої локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getDisplayScript(string $locale, ?string $displayLocale = null): string|false
```

Процедурний стиль

```methodsynopsis
locale_get_display_script(string $locale, ?string $displayLocale = null): string|false
```

Повертає відповідним чином локалізовану назву алфавіту для заданої локалі. Якщо **`null`**, то буде використано локаль за замовчуванням.

### Список параметрів

`locale`

Локаль.

`displayLocale`

Необов'язковий локаль для форматування

### Значення, що повертаються

Назва алфавіту для `locale` у форматі локалі `displayLocale` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                      |
|--------|-----------------------------------------------|
|        | `displayLocale` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **localegetdisplayscript()****

```php
<?php
echo locale_get_display_script('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_script('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_script('sl-Latn-IT-nedis', 'de');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getDisplayScript('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayScript('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayScript('sl-Latn-IT-nedis', 'de');
?>
```

Результат виконання цього прикладу:

```
Latin;
latin;
Lateinisch
```

### Дивіться також

-   [localegetdisplayname()](locale.getdisplayname.md) - Повертає відповідним чином локалізоване ім'я локалі
-   [localegetdisplaylanguage()](locale.getdisplaylanguage.md) - Повертає відповідним чином локалізоване ім'я мови для заданої локалі
-   [localegetdisplayregion()](locale.getdisplayregion.md) - Повертає відповідним чином локалізовану назву регіону для заданої локалі
-   [localegetdisplayvariant()](locale.getdisplayvariant.md) - Повертає відповідним чином локалізовану назву варіанта для заданої локалі