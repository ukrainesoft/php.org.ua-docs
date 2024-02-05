---
navigation:
  - yac.flush.md: '« Yac::flush'
  - yac.getter.md: 'Yac::\_\_get »'
  - index.md: PHP Manual
  - class.yac.md: Yac
title: 'Yac::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yac::get

(PECL yac >= 1.0.0)

Yac::get — Витягує значення з кешу

### Опис

```methodsynopsis
public Yac::get(string|array $key, int &$cas = null): mixed
```

Витягує значення з кешу

### Список параметрів

`key`

Ключ (string) або масив (array), що складається з кількох ключів

`cas`

Якщо не **`null`**, буде встановлено регістр вилучених елементів.

### Значення, що повертаються

Змішане значення у разі успішного виконання, false у разі виникнення помилки
