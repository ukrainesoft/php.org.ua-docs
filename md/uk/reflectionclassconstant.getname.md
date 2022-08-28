Отримати ім'я константи

-   [« ReflectionClassConstant::getModifiers](reflectionclassconstant.getmodifiers.html)
    
-   [ReflectionClassConstant::getValue »](reflectionclassconstant.getvalue.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClassConstant](class.reflectionclassconstant.html)
    
-   Отримати ім'я константи
    

# ReflectionClassConstant::getName

(PHP 7> = 7.1.0, PHP 8)

ReflectionClassConstant::getName — Отримати ім'я константи

### Опис

```methodsynopsis
public ReflectionClassConstant::getName(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я константи.

### список змін

| Версия | Описание |
| --- | --- |
|  | Викидає помилку [Error](class.error.html) якщо властивість name не була ініціалізована. Раніше, у разі помилки, метод повертав **`false`** |