Експорт відбитого методу

-   [« ReflectionMethod::construct](reflectionmethod.construct.html)
    
-   [ReflectionMethod::getClosure »](reflectionmethod.getclosure.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionMethod](class.reflectionmethod.html)
    
-   Експорт відбитого методу
    

# ReflectionMethod::export

(PHP 5, PHP 7)

ReflectionMethod::export — Експорт відбитого методу

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionMethod::export(string $class, string $name, bool $return = false): string
```

Експортує ReflectionMethod.

### Список параметрів

`class`

Назва класу.

`name`

Ім'я методу.

`return`

Встановлення в **`true`** поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return` встановлений в **`true`**, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Дивіться також

-   [ReflectionMethod::construct()](reflectionmethod.construct.html) - Конструктор класу ReflectionMethod
-   [ReflectionMethod::toString()](reflectionmethod.tostring.html) - Повертає рядкову виставу об'єкта ReflectionMethod