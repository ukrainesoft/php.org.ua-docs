---
navigation:
  - locale.getdisplaylanguage.md: '« Locale::getDisplayLanguage'
  - locale.getdisplayregion.md: 'Locale::getDisplayRegion »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getDisplayName'
---
# Locale::getDisplayName

# localegetdisplayname

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getDisplayName -- localegetdisplayname - Повертає відповідним чином локалізоване ім'я локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getDisplayName(string $locale, ?string $displayLocale = null): string|false
```

Процедурний стиль

```methodsynopsis
locale_get_display_name(string $locale, ?string $displayLocale = null): string|false
```

Повертає відповідним чином ім'я локалізоване локалі. Якщо `locale` одно **`null`**, то буде використано локаль за замовчуванням.

### Список параметрів

`locale`

Локаль.

`displayLocale`

Необов'язковий локаль для форматування

### Значення, що повертаються

Ім'я локалі у форматі локалі `displayLocale` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `displayLocale` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **localegetdisplayname()****

```php
<?php
echo locale_get_display_name('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_name('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_name('sl-Latn-IT-nedis', 'de');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getDisplayName('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayName('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayName('sl-Latn-IT-nedis', 'de');
?>
```

Результат виконання цього прикладу:

```
Slovenian (Latin, Italy, Natisone dialect);
slov\xc3\xa8ne (latin, Italie, dialecte de Natisone;
Slowenisch (Lateinisch, Italien, NEDIS)
```

### Дивіться також

-   [localegetdisplaylanguage()](locale.getdisplaylanguage.md) - Повертає відповідним чином локалізоване ім'я мови для заданої локалі
-   [localegetdisplayscript()](locale.getdisplayscript.md) - Повертає відповідним чином локалізовану назву алфавіту для заданої локалі
-   [localegetdisplayregion()](locale.getdisplayregion.md) - Повертає відповідним чином локалізовану назву регіону для заданої локалі
-   [localegetdisplayvariant()](locale.getdisplayvariant.md) - Повертає відповідним чином локалізовану назву варіанта для заданої локалі
