- [« Приклади](intl.examples.md)
- [Collator »](class.collator.md)

- [PHP Manual](index.md)
- [Приклади](intl.examples.md)
- Основи використання модуля

## Основи використання модуля

Кожен модуль надає два типи API: процедурний та
об'єктно-орієнтований. Вони ідентичні та описуються у відповідних
розділи керівництва.

> **Примітка**:
>
> Усі вхідні дані повинні бути у кодуванні UTF-8. Усі вихідні дані
> також.

**Приклад #1 Приклад використання процедурного API**

` <?php$coll  = collator_create('en_US');$result = collator_compare($coll, "string#1", "string#2");?> `

**Приклад #2 Приклад використання об'єктно-орієнтованого API**

` <?php$coll = new Collator('en_US');$al  = $coll->getLocale(Locale::ACTUAL_LOCALE);echo "Поточна локаль: $al
";$formatter = new NumberFormatter('en_US', NumberFormatter::DECIMAL);echo $formatter->format(1234567);?> `
