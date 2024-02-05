---
navigation:
  - intl.examples.md: « Приклади
  - class.collator.md: Collator »
  - index.md: PHP Manual
  - intl.examples.md: Приклади
title: Основи використання модуля
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Основи використання модуля

Кожен модуль надає два типи API: процедурний та об'єктно-орієнтований. Вони ідентичні та описуються у відповідних розділах керівництва.

> **Зауваження** :
> 
> Усі вхідні дані мають бути у кодуванні UTF-8. Всі вихідні дані також.

**Приклад #1 Приклад використання процедурного API**

```php
<?php
$coll  = collator_create('en_US');
$result = collator_compare($coll, "string#1", "string#2");
?>
```

**Приклад #2 Приклад використання об'єктно-орієнтованого API**

```php
<?php
$coll = new Collator('en_US');
$al   = $coll->getLocale(Locale::ACTUAL_LOCALE);
echo "Текущая локаль: $al\n";

$formatter = new NumberFormatter('en_US', NumberFormatter::DECIMAL);
echo $formatter->format(1234567);
?>
```
