---
navigation:
  - reflectionclass.construct.html: '« ReflectionClass::construct'
  - reflectionclass.getattributes.html: 'ReflectionClass::getAttributes »'
  - index.html: PHP Manual
  - class.reflectionclass.html: ReflectionClass
title: 'ReflectionClass::export'
---
# ReflectionClass::export

(PHP 5, PHP 7)

ReflectionClass::export — Експортує клас

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionClass::export(mixed $argument, bool $return = false): string
```

Експортує reflected (відбитий) клас.

### Список параметрів

`argument`

Експортований об'єкт Reflection.

`return`

Встановлення в **`true`** поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return` встановлений в **`true`**, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::export()****

```php
<?php
class Apple {
    public $var1;
    public $var2 = 'Orange';

    public function type() {
        return 'Apple';
    }
}
ReflectionClass::export('Apple');
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Class [ <user> class Apple ] {
  @@ php shell code 1-8

  - Constants [0] {
  }

  - Static properties [0] {
  }

  - Static methods [0] {
  }

  - Properties [2] {
    Property [ <default> public $var1 ]
    Property [ <default> public $var2 ]
  }

  - Methods [1] {
    Method [ <user> public method type ] {
      @@ php shell code 5 - 7
    }
  }
}
```

### Дивіться також

-   [ReflectionClass::getName()](reflectionclass.getname.html) - Повертає ім'я класу
-   [ReflectionClass::toString()](reflectionclass.tostring.html) - Повертає рядкову виставу об'єкта класу ReflectionClass
