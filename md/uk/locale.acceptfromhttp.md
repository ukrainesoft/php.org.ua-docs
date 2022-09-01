---
navigation:
  - class.locale.md: « Locale
  - locale.canonicalize.md: 'Locale::canonicalize »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::acceptFromHttp'
---
# Locale::acceptFromHttp

# localeacceptfromhttp

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::acceptFromHttp -- localeacceptfromhttp — Спробувати визначити найкращу локаль на основі заголовку HTTP "Accept-Language"

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::acceptFromHttp(string $header): string|false
```

Процедурний стиль

```methodsynopsis
locale_accept_from_http(string $header): string|false
```

Намагається визначити локаль, що відповідає списку мов, запрошеному в HTTP-заголовку "Accept-Language".

### Список параметрів

`header`

Рядок, що містить заголовок "Accept-Language" відповідно до формату RFC 2616.

### Значення, що повертаються

Ідентифікатор локалі.

Повертає \*\*`false`\*\*якщо довжина `header` перевищує **`INTL_MAX_LOCALE_LEN`**

### Приклади

**Приклад #1 Приклад використання **localeacceptfromhttp()****

```php
<?php
$locale = locale_accept_from_http($_SERVER['HTTP_ACCEPT_LANGUAGE']);
echo $locale;
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$locale = Locale::acceptFromHttp($_SERVER['HTTP_ACCEPT_LANGUAGE']);
echo $locale;
?>
```

Результат виконання цього прикладу:

```
en_US
```

### Дивіться також

-   [localelookup()](locale.lookup.md) - Пошук мовних позначок найбільш відповідних заданої локалі
