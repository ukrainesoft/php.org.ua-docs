---
navigation:
  - function.ps-set-text-pos.md: « ps\_set\_text\_pos
  - function.ps-setcolor.md: ps\_setcolor »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_set\_value
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_set\_value

(PECL ps >= 1.1.0)

ps\_set\_value — Встановлює певні значення

### Опис

```methodsynopsis
ps_set_value(resource $psdoc, string $name, float $value): bool
```

Встановлює декілька значень, що використовуються багатьма функціями. Параметри визначення є значеннями з плаваючою точкою.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`name`

Значение`name` може бути одне з наступного:

textrendering

Спосіб відображення тексту.

textx

Координата X для виведення тексту.

texty

Координата Y для виведення тексту.

wordspacing

Відстань між словами щодо ширини пробілу.

leading

Відстань між рядками у пікселях.

`value`

Значення параметра.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_get\_value()](function.ps-get-value.md) \- Отримує певні значення
-   [ps\_set\_parameter()](function.ps-set-parameter.md) \- Встановлює певні параметри
