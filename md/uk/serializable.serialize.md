---
navigation:
  - class.serializable.md: « Serializable
  - serializable.unserialize.md: 'Serializable::unserialize »'
  - index.md: PHP Manual
  - class.serializable.md: Serializable
title: 'Serializable::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Serializable::serialize

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

Serializable::serialize — Представляє об'єкт у вигляді рядка

### Опис

```methodsynopsis
public Serializable::serialize(): ?string
```

Повертає рядкову виставу об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу об'єкта або **`null`**

### Помилки

Викидає виняток [Exception](class.exception.md) при поверненні типів, відмінних від рядка або **`null`**

### Дивіться також

-   [\_\_sleep()](language.oop5.magic.md#object.sleep)
-   [\_\_serialize()](language.oop5.magic.md#object.serialize)
