---
navigation:
  - arrayaccess.offsetset.md: '« ArrayAccess::offsetSet'
  - class.serializable.md: Serializable »
  - index.md: PHP Manual
  - class.arrayaccess.md: ArrayAccess
title: 'ArrayAccess::offsetUnset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayAccess::offsetUnset

(PHP 5, PHP 7, PHP 8)

ArrayAccess::offsetUnset — Видаляє зміщення

### Опис

```methodsynopsis
public ArrayAccess::offsetUnset(mixed $offset): void
```

Видаляє зміщення (ключ).

> **Зауваження** :
> 
> Цей метод *не* буде викликаний при наведенні типу до [(unset)](language.types.type-juggling.md#language.types.typecasting)

### Список параметрів

`offset`

Усунення (ключ) для видалення.

### Значення, що повертаються

Функція не повертає значення після виконання.
