---
navigation:
  - locale.composelocale.md: '« Locale::composeLocale'
  - locale.getallvariants.md: 'Locale::getAllVariants »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::filterMatches'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::filterMatches

# locale\_filter\_matches

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::filterMatches -- locale\_filter\_matches — Перевірити, чи відповідає тег фільтра мови локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::filterMatches(string $languageTag, string $locale, bool $canonicalize = false): ?bool
```

Процедурний стиль

```methodsynopsis
locale_filter_matches(string $langtag, string $locale, bool $canonicalize = false): ?bool
```

Перевірити, чи відповідає фільтр `languageTag` локалі `locale` керуючись базовими фільтруючими алгоритмами RFC 4647

### Список параметрів

`languageTag`

Мовний тег

`locale`

Локаль

`canonicalize`

Якщо **`true`**, аргумент буде перетворено до канонічної форми перед перевіркою.

### Значення, що повертаються

**`true`** якщо `locale`подходит для`languageTag`, или\*\*`false`\*\*, якщо ні.

Повертає \*\*`null`\*\*якщо довжина `locale` перевищує **`INTL_MAX_LOCALE_LEN`**

### Приклади

**Приклад #1 Приклад використання** locale\_filter\_matches()\*\*\*\*

```php
<?php
echo (locale_filter_matches('de-DEVA','de-DE', false)) ? "Подходит" : "Не подходит";
echo '; ';
echo (locale_filter_matches('de-DE_1996','de-DE', false)) ? "Подходит" : "Не подходит";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo (Locale::filterMatches('de-DEVA','de-DE', false)) ? "Подходит" : "Не подходит";
echo '; ';
echo (Locale::filterMatches('de-DE-1996','de-DE', false)) ? "Подходит" : "Не подходит";
?>
```

Результат виконання наведеного прикладу:

```
Не подходит; Подходит
```

### Дивіться також

-   [locale\_lookup()](locale.lookup.md) \- Пошук мовних позначок найбільш відповідних заданої локалі
