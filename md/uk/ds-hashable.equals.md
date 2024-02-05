---
navigation:
  - class.ds-hashable.md: « Ds\\Hashable
  - ds-hashable.hash.md: 'Ds\\Hashable::hash »'
  - index.md: PHP Manual
  - class.ds-hashable.md: Ds\\Hashable
title: 'Ds\\Hashable::equals'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Hashable::equals

(PECL ds >= 1.0.0)

Ds\\Hashable::equals — Визначає, чи дорівнює поточний екземпляр переданому об'єкту

### Опис

```methodsynopsis
abstract public Ds\Hashable::equals(object $obj): bool
```

Визначає, чи поточний екземпляр є еквівалентним переданому іншому об'єкту.

Цей метод дозволяє використовувати об'єкти як ключі в таких структурах, як [Ds\\Map](class.ds-map.md) і [Ds\\Set](class.ds-set.md) або будь-які інші структури, що розпізнають цей інтерфейс.

> **Зауваження** :
> 
> Гарантує, що `obj` є екземпляром того самого класу.

**Застереження**

Щоб об'єкти вважалися ідентичними, необхідно, щоб вони мали однаковий хеш. Дивіться опис функції [Ds\\Hashable::hash()](ds-hashable.hash.md)

### Список параметрів

`obj`

Об'єкт порівняння з поточним об'єктом.

### Значення, що повертаються

**`true`**, якщо ідентичні, **`false`** в іншому випадку.
