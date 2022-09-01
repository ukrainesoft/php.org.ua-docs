---
navigation:
  - locale.getdefault.html: '« Locale::getDefault'
  - locale.getdisplayname.html: 'Locale::getDisplayName »'
  - index.html: PHP Manual
  - class.locale.html: Locale
title: 'Locale::getDisplayLanguage'
---
# Locale::getDisplayLanguage

# localegetdisplaylanguage

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getDisplayLanguage -- localegetdisplaylanguage — Повертає відповідним чином локалізоване ім'я мови для заданої локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getDisplayLanguage(string $locale, ?string $displayLocale = null): string|false
```

Процедурний стиль

```methodsynopsis
locale_get_display_language(string $locale, ?string $displayLocale = null): string|false
```

Повертає відповідним чином локалізоване ім'я мови для заданої локалі. Якщо **`null`**, то буде використано локаль за замовчуванням.

### Список параметрів

`locale`

Локаль, для якої буде повернуто назву мови

`displayLocale`

Необов'язковий параметр, що задає локаль, у якій потрібно буде відобразити назву

### Значення, що повертаються

Назва мови для локалі `locale` у форматі, що відповідає локалі `displayLocale` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `displayLocale` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **localegetdisplaylanguage()****

```php
<?php
echo locale_get_display_language('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_language('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_language('sl-Latn-IT-nedis', 'de');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getDisplayLanguage('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayLanguage('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayLanguage('sl-Latn-IT-nedis', 'de');
?>
```

Результат виконання цього прикладу:

```
Slovenian;
slov\xc3\xa8ne;
Slowenisch
```

### Дивіться також

-   [localegetdisplayname()](locale.getdisplayname.html) - Повертає відповідним чином локалізоване ім'я локалі
-   [localegetdisplayscript()](locale.getdisplayscript.html) - Повертає відповідним чином локалізовану назву алфавіту для заданої локалі
-   [localegetdisplayregion()](locale.getdisplayregion.html) - Повертає відповідним чином локалізовану назву регіону для заданої локалі
-   [localegetdisplayvariant()](locale.getdisplayvariant.html) - Повертає відповідним чином локалізовану назву варіанта для заданої локалі
