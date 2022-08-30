Перевірити, чи тег фільтра мови локалі відповідає

-   [« Locale::composeLocale](locale.composelocale.html)
    
-   [Locale::getAllVariants »](locale.getallvariants.html)
    
-   [PHP Manual](index.html)
    
-   [Locale](class.locale.html)
    
-   Перевірити, чи тег фільтра мови локалі відповідає
    

# Locale::filterMatches

# localefiltermatches

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::filterMatches -- localefiltermatches — Перевірити, чи відповідає тег фільтра мови локалі

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

**`true`** якщо `locale` підходить для `languageTag`, або **`false`**, якщо ні.

Повертає \*\*`null`\*\*якщо довжина `locale` перевищує **`INTL_MAX_LOCALE_LEN`**

### Приклади

**Приклад #1 Приклад використання **localefiltermatches()****

```php
<?php
echo (locale_filter_matches('de-DEVA','de-DE', false)) ? "Подходит" : "Не подходит";
echo '; ';
echo (locale_filter_matches('de-DE_1996','de-DE', false)) ? "Подходит" : "Не подходит";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo (Locale::filterMatches('de-DEVA','de-DE', false)) ? "Подходит" : "Не подходит";
echo '; ';
echo (Locale::filterMatches('de-DE-1996','de-DE', false)) ? "Подходит" : "Не подходит";
?>
```

Результат виконання цього прикладу:

```
Не подходит; Подходит
```

### Дивіться також

-   [localelookup()](locale.lookup.html) - Пошук мовних позначок найбільш відповідних заданої локалі