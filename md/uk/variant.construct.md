---
navigation:
  - class.variant.html: « variant
  - class.compersisthelper.html: COMPersistHelper »
  - index.html: PHP Manual
  - class.variant.html: variant
title: 'variant:construct'
---
# variant:construct

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

variant:construct - Конструктор класу variant

### Опис

public **variant:construct**[mixed](language.types.declarations.html#language.types.declarations.mixed) `$value` **`null`**, int `$type` **`VT_EMPTY`**, int `$codepage` **`CP_ACP`**

Створює об'єкт класу variant.

### Список параметрів

`value`

Початкове значення. Якщо не задано або задано як **`null`**, буде створено об'єкт VTEMPTY.

`type`

Визначає тип контенту об'єкта variant. Допустимі значення - одна з констант **`VT_XXX`** [Обумовлені константи](com.constants.html)). PHP може автоматично визначати параметри, передані за посиланням; їх навіть не потрібно передавати як об'єкти variant. Додаткову інформацію за типами variant читайте у бібліотеці MSDN.

`codepage`

Кодова сторінка Подробиці читайте на сторінці [com](class.com.html)
