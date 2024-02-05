---
navigation:
  - reflectionclass.construct.md: '« ReflectionClass::\_\_construct'
  - reflectionclass.getattributes.md: 'ReflectionClass::getAttributes »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::export'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::export

(PHP 5, PHP 7)

ReflectionClass::export — Експортує клас

**Увага**

Ця функція *ЗАСТАРІЛА* починаючи з PHP 7.4.0 і була *ВИДАЛЕНО* у PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionClass::export(mixed $argument, bool $return = false): string
```

Експортує reflected (відбитий) клас.

### Список параметрів

`argument`

Експортований об'єкт Reflection.

`return`

Установка в\*\*`true`\*\* поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return`установлен в\*\*`true`\*\*, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::export()\*\*\*\*

```php
<?php
class Apple {
    public $var1;
    public $var2 = 'Orange';

    public function type() {
        return 'Apple';
    }
}
ReflectionClass::export('Apple');
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [ReflectionClass::getName()](reflectionclass.getname.md) \- Повертає ім'я класу
-   [ReflectionClass::\_\_toString()](reflectionclass.tostring.md) \- Повертає рядкову виставу об'єкта класу ReflectionClass
