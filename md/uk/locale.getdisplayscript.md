---
navigation:
  - locale.getdisplayregion.md: '« Locale::getDisplayRegion'
  - locale.getdisplayvariant.md: 'Locale::getDisplayVariant »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getDisplayScript'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::getDisplayScript

# locale\_get\_display\_script

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getDisplayScript -- locale\_get\_display\_script — Повертає відповідним чином локалізовану назву алфавіту для заданої локалі

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

Название алфавита для`locale`в формате локали`displayLocale`или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `displayLocale` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** locale\_get\_display\_script()\*\*\*\*

```php
<?php
echo locale_get_display_script('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_script('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_script('sl-Latn-IT-nedis', 'de');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo Locale::getDisplayScript('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayScript('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayScript('sl-Latn-IT-nedis', 'de');
?>
```

Результат виконання наведеного прикладу:

```
Latin;
latin;
Lateinisch
```

### Дивіться також

-   [locale\_get\_display\_name()](locale.getdisplayname.md) \- Повертає відповідним чином локалізоване ім'я локалі
-   [locale\_get\_display\_language()](locale.getdisplaylanguage.md) \- Повертає відповідним чином локалізоване ім'я мови для заданої локалі
-   [locale\_get\_display\_region()](locale.getdisplayregion.md) \- Повертає відповідним чином локалізовану назву регіону для заданої локалі
-   [locale\_get\_display\_variant()](locale.getdisplayvariant.md) \- Повертає відповідним чином локалізовану назву варіанта для заданої локалі
