Експорт

-   [« ReflectionProperty::construct](reflectionproperty.construct.html)
    
-   [ReflectionProperty::getAttributes »](reflectionproperty.getattributes.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionProperty](class.reflectionproperty.html)
    
-   Експорт
    

# ReflectionProperty::export

(PHP 5, PHP 7)

ReflectionProperty::export — Експорт

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionProperty::export(mixed $class, string $name, bool $return = ?): string
```

Експортує відображення (reflection).

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`argument`

Експортований об'єкт Reflection.

`name`

Ім'я якості.

`return`

Встановлення в **`true`** поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

### Дивіться також

-   [ReflectionProperty::toString()](reflectionproperty.tostring.html) - Перетворення на рядок