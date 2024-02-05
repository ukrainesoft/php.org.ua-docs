---
navigation:
  - class.reflectionclassconstant.md: « ReflectionClassConstant
  - reflectionclassconstant.export.md: 'ReflectionClassConstant::export »'
  - index.md: PHP Manual
  - class.reflectionclassconstant.md: ReflectionClassConstant
title: 'ReflectionClassConstant::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClassConstant::\_\_construct

(PHP 7 >= 7.1.0, PHP 8)

ReflectionClassConstant::\_\_construct — Створює об'єкт ReflectionClassConstant

### Опис

public **ReflectionClassConstant::\_\_construct**(object|string`$class`, string`$constant`) .

Створює новий об'єкт [ReflectionClassConstant](class.reflectionclassconstant.md)

### Список параметрів

`class`

Рядок (string), що містить ім'я класу для відображення, або об'єкт (object).

`constant`

Ім'я константи класу.

### Помилки

Викидає [Exception](class.exception.md) якщо передана константа класу немає.

### Дивіться також

-   [Конструктори](language.oop5.decon.md#language.oop5.decon.constructor)
