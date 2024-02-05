---
navigation:
  - reference.componere.md: « Функції Componere
  - componere.cast_by_ref.md: Componere\\cast\_by\_ref »
  - index.md: PHP Manual
  - reference.componere.md: Функції Componere
title: Componere\\cast
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\cast

(Componere 2 >= 2.1.2)

Componere\\cast — Приведення до типу

### Опис

```methodsynopsis
Componere\cast(Type $type,  $object): Type
```

### Список параметрів

`type`

Користувальницький тип

`object`

Об'єкт з типом користувача, сумісний з **Type**

### Значення, що повертаються

object типа**Type**, наведений з `object`

### Помилки

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), якщо тип `object` є похідним від внутрішнього класу

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), якщо **Type** є інтерфейсом

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), якщо **Type** є трейтом

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), якщо **Type** є абстрактним класом

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), якщо **Type** не сумісний з типом `object`

### Дивіться також

-   [Componere\\cast\_by\_ref](componere.cast_by_ref.md)
