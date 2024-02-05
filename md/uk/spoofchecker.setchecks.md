---
navigation:
  - spoofchecker.setallowedlocales.md: '« Spoofchecker::setAllowedLocales'
  - spoofchecker.setrestrictionlevel.md: 'Spoofchecker::setRestrictionLevel »'
  - index.md: PHP Manual
  - class.spoofchecker.md: Spoofchecker
title: 'Spoofchecker::setChecks'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Spoofchecker::setChecks

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Spoofchecker::setChecks — Встановити набір перевірок

### Опис

```methodsynopsis
public Spoofchecker::setChecks(int $checks): void
```

Встановлює перевірки, які виконуватимуться методом [SpoofChecker::isSuspicious()](spoofchecker.issuspicious.md)

### Список параметрів

`checks`

Перевірки, які виконуватимуться методом [SpoofChecker::isSuspicious()](spoofchecker.issuspicious.md). Бітова маска, що складається з констант **`Spoofchecker::SINGLE_SCRIPT_CONFUSABLE`** **`Spoofchecker::MIXED_SCRIPT_CONFUSABLE`** **`Spoofchecker::WHOLE_SCRIPT_CONFUSABLE`** **`Spoofchecker::ANY_CASE`** **`Spoofchecker::SINGLE_SCRIPT`** **`Spoofchecker::INVISIBLE`**или**`Spoofchecker::CHAR_LIMIT`**. За промовчанням всі перевірки, починаючи з ICU 58; до цієї версії константа **`Spoofchecker::SINGLE_SCRIPT`** була виключена.

### Значення, що повертаються

Функція не повертає значення після виконання.
