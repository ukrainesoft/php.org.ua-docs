---
navigation:
  - componere.cast.md: « Componere\\cast
  - book.errorfunc.md: Обробка помилок "
  - index.md: PHP Manual
  - reference.componere.md: Функції Componere
title: Componere\\cast\_by\_ref
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\cast\_by\_ref

(Componere 2 >= 2.1.2)

Componere\\cast\_by\_ref — Приведення до типу

### Опис

```methodsynopsis
Componere\cast_by_ref(Type $type,  $object): Type
```

### Список параметрів

**type**

Користувальницький тип

`object`

Об'єкт з типом користувача, сумісним з **Type**

### Значення, що повертаються

object типа**Type**, наведений з `object`де елементи є посиланнями на елементи `object`

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

-   [Componere\\cast](componere.cast.md)
