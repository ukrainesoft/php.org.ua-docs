Отримати ім'я константи

-   [« ReflectionClassConstant::getModifiers](reflectionclassconstant.getmodifiers.md)
    
-   [ReflectionClassConstant::getValue »](reflectionclassconstant.getvalue.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionClassConstant](class.reflectionclassconstant.md)
    
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
|  | Викидає помилку [Error](class.error.md) якщо властивість name не була ініціалізована. Раніше, у разі помилки, метод повертав **`false`** |