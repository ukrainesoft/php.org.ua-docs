---
navigation:
  - splfixedarray.getsize.md: '« SplFixedArray::getSize'
  - splfixedarray.key.md: 'SplFixedArray::key »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::jsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFixedArray::jsonSerialize

(PHP 8 >= 8.1.0)

SplFixedArray::jsonSerialize — Повертає уявлення, яке може бути перетворене на JSON

### Опис

```methodsynopsis
public SplFixedArray::jsonSerialize(): mixed
```

Серіалізує масив у значення, яке може бути серіалізовано нативно за допомогою функції [json\_encode()](function.json-encode.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив даних, який може бути серіалізований функцією [json\_encode()](function.json-encode.md), Що являє собою значення будь-якого типу, відмінного від ресурсу ([resource](language.types.resource.md)
