---
navigation:
  - class.variant.md: « variant
  - class.compersisthelper.md: COMPersistHelper »
  - index.md: PHP Manual
  - class.variant.md: variant
title: 'variant::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant::\_\_construct

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

variant::\_\_construct - Конструктор класу variant

### Опис

public **variant::\_\_construct** [mixed](language.types.declarations.md#language.types.declarations.mixed) `$value` **`null`**, int`$type` **`VT_EMPTY`**, int`$codepage` **`CP_ACP`**) .

Створює об'єкт класу variant.

### Список параметрів

`value`

Початкове значення. Якщо не задано або задано як **`null`**, буде створено об'єкт VT\_EMPTY.

`type`

Визначає тип контенту об'єкта variant. Допустимі значення - одна з констант **`VT_XXX`** [Обумовлені константи](com.constants.md) ). PHP може автоматично визначати параметри, передані за посиланням; їх навіть не потрібно передавати як об'єкти variant. Додаткову інформацію за типами variant читайте у бібліотеці MSDN.

`codepage`

Кодова сторінка Подробиці читайте на сторінці [com](class.com.md)
