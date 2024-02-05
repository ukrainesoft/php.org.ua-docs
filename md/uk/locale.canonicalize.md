---
navigation:
  - locale.acceptfromhttp.md: '« Locale::acceptFromHttp'
  - locale.composelocale.md: 'Locale::composeLocale »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::canonicalize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::canonicalize

# locale\_canonicalize

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::canonicalize -- locale\_canonicalize — Канонізувати рядок локалі

### Опис

```methodsynopsis
public static Locale::canonicalize(string $locale): ?string
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`locale`

### Значення, що повертаються

Канонізований рядок локалі.

Повертає \*\*`null`\*\*якщо довжина `locale` перевищує **`INTL_MAX_LOCALE_LEN`**
