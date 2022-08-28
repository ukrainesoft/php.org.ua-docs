Повертає константи

-   [« ReflectionClass::getConstant](reflectionclass.getconstant.html)
    
-   [ReflectionClass::getConstructor »](reflectionclass.getconstructor.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Повертає константи
    

# ReflectionClass::getConstants

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getConstants — Повертає константи

### Опис

```methodsynopsis
public ReflectionClass::getConstants(?int $filter = null): array
```

Повертає всі визначені класі константи, незалежно від своїх модифікаторів видимості.

### Список параметрів

`filter`

Додатковий фільтр для фільтрації констант видимості. Він налаштовується за допомогою [ReflectionClassConstant constants](class.reflectionclassconstant.html#reflectionclassconstant.constants.modifiers) і за умовчанням використовується всім констант видимості.

### Значення, що повертаються

Масив (array) констант. Ім'я константи – ключ, значення константи – значення.

### список змін

| Версия | Описание                  |
|--------|---------------------------|
|        | Доданий параметр `filter` |

### Дивіться також

-   [ReflectionClass::getConstant()](reflectionclass.getconstant.html) - Повертає певну константу