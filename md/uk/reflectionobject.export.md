Експорт

-   [« ReflectionObject::construct](reflectionobject.construct.md)
    
-   [ReflectionParameter »](class.reflectionparameter.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionObject](class.reflectionobject.md)
    
-   Експорт
    

# ReflectionObject::export

(PHP 5, PHP 7)

ReflectionObject::export — Експорт

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionObject::export(string $argument, bool $return = ?): string
```

Експортує відображення (reflection).

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`argument`

Експортований об'єкт Reflection.

`return`

Встановлення в **`true`** поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return` встановлений в **`true`**, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Дивіться також

-   [ReflectionObject::construct()](reflectionobject.construct.md) - Конструктор класу ReflectionObject