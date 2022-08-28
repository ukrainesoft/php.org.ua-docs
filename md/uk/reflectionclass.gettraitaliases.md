Повертає масив псевдонімів трейтів

-   [« ReflectionClass::getStaticPropertyValue](reflectionclass.getstaticpropertyvalue.html)
    
-   [ReflectionClass::getTraitNames »](reflectionclass.gettraitnames.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Повертає масив псевдонімів трейтів
    

# ReflectionClass::getTraitAliases

(PHP 5> = 5.4.0, PHP 7, PHP 8)

ReflectionClass::getTraitAliases — Повертає масив псевдонімів трейтів

### Опис

```methodsynopsis
public ReflectionClass::getTraitAliases(): array
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив, ключами якого є нові імена методів, а значеннями - оригінальні імена методів (у форматі `"TraitName::original"`). У разі виникнення помилки повертає **`null`**