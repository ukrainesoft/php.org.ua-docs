Приведення до типу

-   [« Функции Componere](reference.componere.html)
    
-   [Componerecastбref »](componere.cast_by_ref.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Componere](reference.componere.html)
    
-   Приведення до типу
    

# Componerecast

(Componere 2 >= 2.1.2)

Componerecast — Приведення до типу

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

object типу **Type**, наведений з `object`

### Помилки

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.html), якщо тип `object` є похідним від внутрішнього класу

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.html), якщо **Type** є інтерфейсом

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.html), якщо **Type** є трейтом

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.html), якщо **Type** є абстрактним класом

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.html), якщо **Type** не сумісний з типом `object`

### Дивіться також

-   [Componerecastбref](componere.cast_by_ref.html)