---
navigation:
  - locale.getscript.md: '« Locale::getScript'
  - locale.parselocale.md: 'Locale::parseLocale »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::lookup'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::lookup

# locale\_lookup

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::lookup -- locale\_lookup — Пошук мовних позначок найбільш відповідних заданої локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::lookup(    array $languageTag,    string $locale,    bool $canonicalize = false,    ?string $defaultLocale = null): ?string
```

Процедурний стиль

```methodsynopsis
locale_lookup(    array $languageTag,    string $locale,    bool $canonicalize = false,    ?string $defaultLocale = null): ?string
```

Шукає елементи `languageTag`, що найкраще підходять для діапазону мов, зазначеного в `locale`, відповідно до алгоритму пошуку RFC 4647

### Список параметрів

`languageTag`

Масив (array), що містить список міток мов для порівняння з `locale`. Не більше 100 елементів.

`locale`

Локаль.

`canonicalize`

Якщо **`true`**, то аргументи спершу будуть приведені до канонічного вигляду.

`defaultLocale`

За умовчанням локаль, якщо збігів не буде знайдено.

### Значення, що повертаються

Найбільш відповідна даної локалі мітка мови.

Повертає \*\*`null`\*\*якщо довжина `locale` перевищує **`INTL_MAX_LOCALE_LEN`**

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | `defaultLocale` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**locale\_lookup()\*\*\*\*

```php
<?php
$arr = array(
    'de-DEVA',
    'de-DE-1996',
    'de',
    'de-De'
);
echo locale_lookup($arr, 'de-DE-1996-x-prv1-prv2', true, 'en_US');
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$arr = array(
    'de-DEVA',
    'de-DE-1996',
    'de',
    'de-De'
);
echo Locale::lookup($arr, 'de-DE-1996-x-prv1-prv2', true, 'en_US');
?>
```

Результат виконання наведеного прикладу:

```
de_de_1996
```

### Дивіться також

-   [locale\_filter\_matches()](locale.filtermatches.md) \- Перевірити, чи тег фільтра мови локалі відповідає
