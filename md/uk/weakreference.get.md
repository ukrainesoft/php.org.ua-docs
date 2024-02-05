---
navigation:
  - weakreference.create.md: '« WeakReference::create'
  - class.weakmap.md: WeakMap »
  - index.md: PHP Manual
  - class.weakreference.md: WeakReference
title: 'WeakReference::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# WeakReference::get

(PHP 7 >= 7.4.0, PHP 8)

WeakReference::get — Отримує об'єкт із слабким посиланням

### Опис

```methodsynopsis
public WeakReference::get(): ?object
```

Отримує об'єкт із слабким посиланням. Якщо об'єкт вже було знищено, повертається **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає посилання object або **`null`**, якщо об'єкт було знищено.
