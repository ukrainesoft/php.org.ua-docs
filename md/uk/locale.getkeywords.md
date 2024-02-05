---
navigation:
  - locale.getdisplayvariant.md: '« Locale::getDisplayVariant'
  - locale.getprimarylanguage.md: 'Locale::getPrimaryLanguage »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getKeywords'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::getKeywords

# locale\_get\_keywords

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getKeywords -- locale\_get\_keywords — Отримати ключові слова для локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getKeywords(string $locale): array|false|null
```

Процедурний стиль

```methodsynopsis
locale_get_keywords(string $locale): array|false|null
```

Отримує ключові слова для локалі.

### Список параметрів

`locale`

Локаль для отримання ключових слів

### Значення, що повертаються

Асоціативний масив (array) з парами ключ-значення для заданої локалі

Повертає \*\*`null`\*\*якщо довжина `locale` перевищує **`INTL_MAX_LOCALE_LEN`**

### Приклади

**Пример #1 Пример использования**locale\_get\_keywords()\*\*\*\*

```php
<?php
$keywords_arr = locale_get_keywords('de_DE@currency=EUR;collation=PHONEBOOK');
if ($keywords_arr) {
    foreach ($keywords_arr as $key => $value) {
        echo "$key = $value\n";
    }
}
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$keywords_arr = Locale::getKeywords('de_DE@currency=EUR;collation=PHONEBOOK');
if ($keywords_arr) {
    foreach ($keywords_arr as $key => $value) {
        echo "$key = $value\n";
    }
}
?>
```

Результат виконання наведеного прикладу:

```
collation = PHONEBOOK
currency = EUR
```

### Дивіться також

-   [locale\_get\_all\_variants()](locale.getallvariants.md) \- Отримання варіантів із переданої локалі
