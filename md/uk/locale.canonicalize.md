---
navigation:
  - locale.acceptfromhttp.md: '« Locale::acceptFromHttp'
  - locale.composelocale.md: 'Locale::composeLocale »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::canonicalize'
---
# Locale::canonicalize

# localecanonicalize

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::canonicalize -- localecanonicalize — Канонізувати рядок локалі

### Опис

```methodsynopsis
public static Locale::canonicalize(string $locale): ?string
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`locale`

### Значення, що повертаються

Канонізований рядок локалі.

Повертає \*\*`null`\*\*якщо довжина `locale` перевищує **`INTL_MAX_LOCALE_LEN`**
