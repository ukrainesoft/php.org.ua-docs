---
navigation:
  - locale.getdisplayscript.md: '« Locale::getDisplayScript'
  - locale.getkeywords.md: 'Locale::getKeywords »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getDisplayVariant'
---
# Locale::getDisplayVariant

# localegetdisplayvariant

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getDisplayVariant -- localegetdisplayvariant — Повертає відповідним чином локалізовану назву варіанта для заданої локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getDisplayVariant(string $locale, ?string $displayLocale = null): string|false
```

Процедурний стиль

```methodsynopsis
locale_get_display_variant(string $locale, ?string $displayLocale = null): string|false
```

Повертає відповідним чином локалізовану назву варіанта для заданої локалі. Якщо **`null`**, то буде використано локаль за замовчуванням.

### Список параметрів

`locale`

Локаль.

`displayLocale`

Необов'язковий локаль для форматування

### Значення, що повертаються

Назва варіанта для `locale` у форматі локалі `displayLocale` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `displayLocale` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **localegetdisplayvariant()****

```php
<?php
echo locale_get_display_variant('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_variant('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_variant('sl-Latn-IT-nedis', 'de');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getDisplayVariant('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayVariant('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayVariant('sl-Latn-IT-nedis', 'de');
?>
```

Результат виконання цього прикладу:

```
Natisone dialect;
dialecte de Natisone;
NEDIS
```

### Дивіться також

-   [localegetdisplayname()](locale.getdisplayname.md) - Повертає відповідним чином локалізоване ім'я локалі
-   [localegetdisplaylanguage()](locale.getdisplaylanguage.md) - Повертає відповідним чином локалізоване ім'я мови для заданої локалі
-   [localegetdisplayscript()](locale.getdisplayscript.md) - Повертає відповідним чином локалізовану назву алфавіту для заданої локалі
-   [localegetdisplayregion()](locale.getdisplayregion.md) - Повертає відповідним чином локалізовану назву регіону для заданої локалі
