Отримує ReflectionClassConstant для константи класу

-   [« ReflectionClass::getProperty](reflectionclass.getproperty.html)
    
-   [ReflectionClass::getReflectionConstants »](reflectionclass.getreflectionconstants.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Отримує ReflectionClassConstant для константи класу
    

# ReflectionClass::getReflectionConstant

(PHP 7> = 7.1.0, PHP 8)

ReflectionClass::getReflectionConstant — Отримує [ReflectionClassConstant](class.reflectionclassconstant.html) для константи класу

### Опис

```methodsynopsis
public ReflectionClass::getReflectionConstant(string $name): ReflectionClassConstant|false
```

Отримує [ReflectionClassConstant](class.reflectionclassconstant.html) для якості константи.

### Список параметрів

`name`

Назва константи класу.

### Значення, що повертаються

Об'єкт [ReflectionClassConstant](class.reflectionclassconstant.html) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ReflectionClass::getReflectionConstants()](reflectionclass.getreflectionconstants.html) - Отримує константи класу
-   [ReflectionClassConstant](class.reflectionclassconstant.html)