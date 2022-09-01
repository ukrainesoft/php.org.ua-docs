---
navigation:
  - quickhashintstringhash.delete.md: '« QuickHashIntStringHash::delete'
  - quickhashintstringhash.get.md: 'QuickHashIntStringHash::get »'
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::exists'
---
# QuickHashIntStringHash::exists

(PECL quickhash >= Unknown)

QuickHashIntStringHash::exists — Метод перевіряє, чи є ключ частиною хеша

### Опис

```methodsynopsis
public QuickHashIntStringHash::exists(int $key): bool
```

Метод перевіряє, чи існує у хеші запис із зазначеним ключем.

### Список параметрів

`key`

Ключ запису для перевірки її існування у хеші.

### Значення, що повертаються

Метод повертає **`true`**, якщо запис було знайдено або **`false`**, якщо запис не знайдено.
