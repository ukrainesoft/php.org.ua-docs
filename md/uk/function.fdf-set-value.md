---
navigation:
  - function.fdf-set-target-frame.html: « fdfsettargetframe
  - function.fdf-set-version.html: fdfsetversion »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsetvalue
---
# fdfsetvalue

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfsetvalue — Встановлює значення поля

### Опис

```methodsynopsis
fdf_set_value(    resource $fdf_document,    string $fieldname,    mixed $value,    int $isName = ?): bool
```

Встановлює `value` для заданого поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) ор [fdfopenstring()](function.fdf-open-string.md)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`value`

Цей параметр зберігатиметься у вигляді рядка, якщо він не є масивом. І тут всі елементи масиву будуть збережені як масив значень.

`isName`

> **Зауваження**
> 
> У старіших версіях набору інструментів FDF останній параметр визначав, чи має значення поля бути перетворено на PDF Name (= 1) чи встановлено PDF String (= 0).
> 
> Це значення більше не використовується у поточній версії 5.0. Для сумісності воно, як і раніше, підтримується як необов'язковий параметр, але внутрішньо ігнорується.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfgetvalue()](function.fdf-get-value.md) - Отримує значення поля
-   [fdfremoveitem()](function.fdf-remove-item.md) - Встановлює цільовий кадр для форми
