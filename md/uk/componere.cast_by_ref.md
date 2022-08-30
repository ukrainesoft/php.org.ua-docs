Приведення до типу

-   [« Componerecast](componere.cast.md)
    
-   [Обработка ошибок »](book.errorfunc.md)
    
-   [PHP Manual](index.md)
    
-   [Функции Componere](reference.componere.md)
    
-   Приведення до типу
    

# Componerecastбref

(Componere 2 >= 2.1.2)

Componerecastбref — Приведення до типу

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

object типу **Type**, наведений з `object`де елементи є посиланнями на елементи `object`

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

-   [Componerecast](componere.cast.md)