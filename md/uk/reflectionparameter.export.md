Експорт

-   [« ReflectionParameter::\_\_construct](reflectionparameter.construct.html)
    
-   [ReflectionParameter::getAttributes »](reflectionparameter.getattributes.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionParameter](class.reflectionparameter.html)
    
-   Експорт
    

# ReflectionParameter::export

(PHP 5, PHP 7)

ReflectionParameter::export — Експорт

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionParameter::export(string $function, string $parameter, bool $return = ?): string
```

Експорт.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`function`

Ім'я функції.

`parameter`

Ім'я аргументу.

`return`

Встановлення в **`true`** поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Експорт відбиття (reflection).

### Дивіться також

-   [ReflectionParameter::\_\_toString()](reflectionparameter.tostring.html) - Перетворення на рядок