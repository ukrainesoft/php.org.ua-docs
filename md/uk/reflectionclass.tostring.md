---
navigation:
  - reflectionclass.setstaticpropertyvalue.md: '« ReflectionClass::setStaticPropertyValue'
  - class.reflectionclassconstant.md: ReflectionClassConstant »
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::function toString() { \[native code\] }'
---
# ReflectionClass::function toString() { \[native code\] }

(PHP 5, PHP 7, PHP 8)

ReflectionClass::toString — Повертає рядкову виставу об'єкта класу ReflectionClass

### Опис

```methodsynopsis
public ReflectionClass::__toString(): string
```

Повертає рядкову виставу об'єкта класу ReflectionClass.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Строкове подання екземпляра класу [ReflectionClass](class.reflectionclass.md)

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::toString()****

```php
<?php
$reflectionClass = new ReflectionClass('Exception');
echo $reflectionClass->__toString();
?>
```

Результат виконання цього прикладу:

```
Class [ <internal:Core> class Exception ] {

  - Constants [0] {
  }

  - Static properties [0] {
  }

  - Static methods [0] {
  }

  - Properties [7] {
    Property [ <default> protected $message ]
    Property [ <default> private $string ]
    Property [ <default> protected $code ]
    Property [ <default> protected $file ]
    Property [ <default> protected $line ]
    Property [ <default> private $trace ]
    Property [ <default> private $previous ]
  }

  - Methods [10] {
    Method [ <internal:Core> final private method __clone ] {
    }

    Method [ <internal:Core, ctor> public method __construct ] {

      - Parameters [3] {
        Parameter #0 [ <optional> $message ]
        Parameter #1 [ <optional> $code ]
        Parameter #2 [ <optional> $previous ]
      }
    }

    Method [ <internal:Core> final public method getMessage ] {
    }

    Method [ <internal:Core> final public method getCode ] {
    }

    Method [ <internal:Core> final public method getFile ] {
    }

    Method [ <internal:Core> final public method getLine ] {
    }

    Method [ <internal:Core> final public method getTrace ] {
    }

    Method [ <internal:Core> final public method getPrevious ] {
    }

    Method [ <internal:Core> final public method getTraceAsString ] {
    }

    Method [ <internal:Core> public method __toString ] {
    }
  }
}
```

### Дивіться також

-   [ReflectionClass::export()](reflectionclass.export.md) - Експортує клас
-   [toString()](language.oop5.magic.md#object.tostring)
