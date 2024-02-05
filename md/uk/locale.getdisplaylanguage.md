---
navigation:
  - locale.getdefault.md: '« Locale::getDefault'
  - locale.getdisplayname.md: 'Locale::getDisplayName »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getDisplayLanguage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::getDisplayLanguage

# locale\_get\_display\_language

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getDisplayLanguage -- locale\_get\_display\_language — Повертає відповідним чином локалізоване ім'я мови для заданої локалі

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

Необов'язковий параметр, що задає локаль, у якій треба буде відобразити назву

### Значення, що повертаються

Назва мови для локалі `locale` у форматі, що відповідає локалі `displayLocale`или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `displayLocale` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**locale\_get\_display\_language()\*\*\*\*

```php
<?php
echo locale_get_display_language('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_language('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_language('sl-Latn-IT-nedis', 'de');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getDisplayLanguage('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayLanguage('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayLanguage('sl-Latn-IT-nedis', 'de');
?>
```

Результат виконання наведеного прикладу:

```
Slovenian;
slov\xc3\xa8ne;
Slowenisch
```

### Дивіться також

-   [locale\_get\_display\_name()](locale.getdisplayname.md) \- Повертає відповідним чином локалізоване ім'я локалі
-   [locale\_get\_display\_script()](locale.getdisplayscript.md) \- Повертає відповідним чином локалізовану назву алфавіту для заданої локалі
-   [locale\_get\_display\_region()](locale.getdisplayregion.md) \- Повертає відповідним чином локалізовану назву регіону для заданої локалі
-   [locale\_get\_display\_variant()](locale.getdisplayvariant.md) \- Повертає відповідним чином локалізовану назву варіанта для заданої локалі
