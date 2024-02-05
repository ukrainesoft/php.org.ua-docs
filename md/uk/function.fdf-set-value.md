---
navigation:
  - function.fdf-set-target-frame.md: « fdf\_set\_target\_frame
  - function.fdf-set-version.md: fdf\_set\_version »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_set\_value
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_set\_value

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_set\_value — Встановлює значення поля

### Опис

```methodsynopsis
fdf_set_value(    resource $fdf_document,    string $fieldname,    mixed $value,    int $isName = ?): bool
```

Устанавливает`value`для заданного поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md)or[fdf\_open\_string()](function.fdf-open-string.md)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`value`

Цей параметр зберігатиметься у вигляді рядка, якщо він не є масивом. І тут всі елементи масиву будуть збережені як масив значень.

`isName`

> **Зауваження** :
> 
> У старіших версіях набору інструментів FDF останній параметр визначав, чи має значення поля бути перетворено на PDF Name (= 1) чи встановлено PDF String (= 0).
> 
> Це значення більше не використовується у поточній версії 5.0. Для сумісності воно, як і раніше, підтримується як необов'язковий параметр, але внутрішньо ігнорується.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fdf\_get\_value()](function.fdf-get-value.md) \- Отримує значення поля
-   [fdf\_remove\_item()](function.fdf-remove-item.md) \- Встановлює цільовий кадр для форми
